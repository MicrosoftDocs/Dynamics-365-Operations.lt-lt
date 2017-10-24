--- 
title: "Dokumentų generavimas elektroninėse ataskaitose (ER) su atnaujintais prašymų duomenimis"
description: "Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (4 dalis – modifikuoti formatą)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b2844621bf50a385ad1a4770c0df2d97623dc77a
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="a9125-103">Dokumentų generavimas elektroninėse ataskaitose (ER) su atnaujintais prašymų duomenimis</span><span class="sxs-lookup"><span data-stu-id="a9125-103">Generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9125-104">Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (4 dalis: modifikuoti formatą)“.</span><span class="sxs-lookup"><span data-stu-id="a9125-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="a9125-105">Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą ir atnaujinti programos duomenis.</span><span class="sxs-lookup"><span data-stu-id="a9125-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="a9125-106">Šioje procedūroje vykdote ER formato konfigūraciją, kad sugeneruotumėte Intrastat ataskaitą ir atnaujintumėte programos duomenis ataskaitų proceso archyvavimo informacijai.</span><span class="sxs-lookup"><span data-stu-id="a9125-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="a9125-107">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="a9125-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="a9125-108">Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="a9125-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="a9125-109">Prieš pradėdami įsitikinkite, kad šalies kontekstas DEMF įmonei yra BEL (Belgija).</span><span class="sxs-lookup"><span data-stu-id="a9125-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="a9125-110">Nustatyti užsienio prekybos parametrus</span><span class="sxs-lookup"><span data-stu-id="a9125-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="a9125-111">Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.</span><span class="sxs-lookup"><span data-stu-id="a9125-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="a9125-112">Spustelėkite skirtuką Numeracijos.</span><span class="sxs-lookup"><span data-stu-id="a9125-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="a9125-113">Archyvuojami Intrastat ataskaitų kūrimo proceso informaciją, turime nustatyti kiekvieno archyvo, kurį sukūrėme, įrašus.</span><span class="sxs-lookup"><span data-stu-id="a9125-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="a9125-114">Tam reikia konfigūruoti specialią numerių seką.</span><span class="sxs-lookup"><span data-stu-id="a9125-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="a9125-115">Pasirinkite „Intrastat archyvo ID“ nuorodą.</span><span class="sxs-lookup"><span data-stu-id="a9125-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="a9125-116">Lauke Numeracijos kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9125-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="a9125-117">Lauke „Numerių sekos kodas“ įveskite arba pasirinkite vertę „Fore_2“.</span><span class="sxs-lookup"><span data-stu-id="a9125-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="a9125-118">ResolveChanges Numerio sekos kodas.</span><span class="sxs-lookup"><span data-stu-id="a9125-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="a9125-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a9125-119">Click Save.</span></span>
7. <span data-ttu-id="a9125-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9125-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="a9125-121">Paleiskite pakeistą ER formatą</span><span class="sxs-lookup"><span data-stu-id="a9125-121">Run modified ER format</span></span>
1. <span data-ttu-id="a9125-122">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="a9125-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a9125-123">Medyje išplėskite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="a9125-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="a9125-124">Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.</span><span class="sxs-lookup"><span data-stu-id="a9125-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="a9125-125">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="a9125-125">Click Run.</span></span>
5. <span data-ttu-id="a9125-126">Lauke Įveskite failo pavadinimą įveskite „intrastat2.xml“.</span><span class="sxs-lookup"><span data-stu-id="a9125-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="a9125-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="a9125-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="a9125-128">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a9125-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="a9125-129">Peržiūrėkite ER formato vykdymo rezultatus</span><span class="sxs-lookup"><span data-stu-id="a9125-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="a9125-130">Peržiūrėkite sugeneruotą XML failą.</span><span class="sxs-lookup"><span data-stu-id="a9125-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="a9125-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9125-131">Close the page.</span></span>
2. <span data-ttu-id="a9125-132">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a9125-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="a9125-133">Atidarykite šią formą, kurioje yra Intrastat operacijos, kurios buvo įtrauktos sugeneruotą elektroninį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="a9125-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="a9125-134">Spustelėkite Intrastat archyvas.</span><span class="sxs-lookup"><span data-stu-id="a9125-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="a9125-135">Kadangi įvykdyto ER formate dabar yra programos duomenų atnaujinimo parametrai, informacija apie užpildytą Intrastat ataskaitą suarchyvuota.</span><span class="sxs-lookup"><span data-stu-id="a9125-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="a9125-136">Šioje formoje galite pamatyti sukurto archyvo antraštės įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9125-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="a9125-137">Spustelėkite Informacija.</span><span class="sxs-lookup"><span data-stu-id="a9125-137">Click Details.</span></span>
    * <span data-ttu-id="a9125-138">Šioje formoje galite pamatyti sukurto archyvo išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="a9125-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="a9125-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9125-139">Close the page.</span></span>
6. <span data-ttu-id="a9125-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9125-140">Close the page.</span></span>
7. <span data-ttu-id="a9125-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9125-141">Close the page.</span></span>


