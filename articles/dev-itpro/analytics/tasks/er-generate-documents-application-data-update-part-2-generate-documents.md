--- 
title: "Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas"
description: "Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (1 dalis – importuoti konfigūracijas)“."
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8376107a33dd83e04f82fcab6847e7f073f08dbc
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="fb3b5-103">Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas</span><span class="sxs-lookup"><span data-stu-id="fb3b5-103">Design configurations to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb3b5-104">Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (1 dalis – importuoti konfigūracijas)“.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-104">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="fb3b5-105">Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="fb3b5-106">Šios procedūros metu vykdoma ER importuota formato konfigūracija, sukurta pavyzdinei įmonei „Litware, Inc.“, kad būtų galima generuoti elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-106">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="fb3b5-107">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="fb3b5-108">Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-108">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="fb3b5-109">Prieš pradėdami pakeisti šalies kontekstą DEMF įmonei iš DEU (Vokietija) į BEL (Belgija).</span><span class="sxs-lookup"><span data-stu-id="fb3b5-109">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="fb3b5-110">Spustelėkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai, kad atnaujintumėte šalies kodą juridinio subjekto DEMF pagrindiniame adrese.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-110">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="fb3b5-111">Paleiskite programą iš naujo.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-111">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="fb3b5-112">Paleiskite importuotą ER formatą</span><span class="sxs-lookup"><span data-stu-id="fb3b5-112">Run imported ER format</span></span>
1. <span data-ttu-id="fb3b5-113">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-113">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fb3b5-114">Medyje išplėskite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-114">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="fb3b5-115">Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-115">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="fb3b5-116">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-116">Click Run.</span></span>
    * <span data-ttu-id="fb3b5-117">Paleiskite ER formato konfigūracijos juodraščio versiją, norėdami generuoti Intrastat ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-117">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="fb3b5-118">Lauke Įveskite failo pavadinimą įveskite „intrastat.xml“.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-118">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="fb3b5-119">Nurodykite failo vardą.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-119">Specify the name of the file.</span></span>  
6. <span data-ttu-id="fb3b5-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-120">Click OK.</span></span>
    * <span data-ttu-id="fb3b5-121">Peržiūrėkite sugeneruotą XML failą.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-121">Review the generated XML file.</span></span>  
7. <span data-ttu-id="fb3b5-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-122">Close the page.</span></span>
8. <span data-ttu-id="fb3b5-123">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-123">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="fb3b5-124">Atidarykite šią formą, kad peržiūrėtumėte Intrastat operacijas, kurios yra įtrauktos sugeneruotą elektroninį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-124">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="fb3b5-125">Spustelėkite Intrastat archyvas.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-125">Click Intrastat archive.</span></span>
    * <span data-ttu-id="fb3b5-126">Kadangi įvykdytame ER formate nėra jokių programos duomenų atnaujinimo parametrų, informacija apie užpildytą Intrastat ataskaitą nesuarchyvuota.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-126">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="fb3b5-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-127">Close the page.</span></span>
11. <span data-ttu-id="fb3b5-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fb3b5-128">Close the page.</span></span>


