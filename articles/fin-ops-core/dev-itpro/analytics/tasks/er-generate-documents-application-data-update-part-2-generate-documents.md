---
title: Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas
description: Šioje temoje aprašoma, kaip kurti elektroninių ataskaitų (ER )konfigūracijas, norint generuoti elektroninį dokumentą. (1 dalis – konfigūracijų importavimas).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563179"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="f30b3-104">Konfigūracijų, skirtų generuoti dokumentus, kuriuose yra prašymų duomenys, kūrimas</span><span class="sxs-lookup"><span data-stu-id="f30b3-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f30b3-105">Norėdami atlikti šios procedūros veiksmus, turite pirma užbaigti procedūrą „ER generuoti dokumentus su programos duomenų atnaujinimu (1 dalis – importuoti konfigūracijas)“.</span><span class="sxs-lookup"><span data-stu-id="f30b3-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="f30b3-106">Veiksmai šioje procedūroje paaiškina, kaip kurti elektroninių ataskaitų (ER) konfigūraciją, norint generuoti elektroninį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="f30b3-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="f30b3-107">Šios procedūros metu vykdoma ER importuota formato konfigūracija, sukurta pavyzdinei įmonei „Litware, Inc.“, kad būtų galima generuoti elektroninius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="f30b3-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="f30b3-108">Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="f30b3-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="f30b3-109">Šiuos veiksmus galima atlikti naudojant DEMF duomenų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f30b3-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="f30b3-110">Prieš pradėdami pakeisti šalies kontekstą DEMF įmonei iš DEU (Vokietija) į BEL (Belgija).</span><span class="sxs-lookup"><span data-stu-id="f30b3-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="f30b3-111">Spustelėkite Organizacijos administravimas > Organizacijos > Juridiniai subjektai, kad atnaujintumėte šalies kodą juridinio subjekto DEMF pagrindiniame adrese.</span><span class="sxs-lookup"><span data-stu-id="f30b3-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="f30b3-112">Paleiskite programą iš naujo.</span><span class="sxs-lookup"><span data-stu-id="f30b3-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="f30b3-113">Paleiskite importuotą ER formatą</span><span class="sxs-lookup"><span data-stu-id="f30b3-113">Run imported ER format</span></span>
1. <span data-ttu-id="f30b3-114">Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="f30b3-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f30b3-115">Medyje išplėskite „Intrastat (model)“.</span><span class="sxs-lookup"><span data-stu-id="f30b3-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="f30b3-116">Medyje pasirinkite „Intrastat (model)\Intrastat (format)“.</span><span class="sxs-lookup"><span data-stu-id="f30b3-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="f30b3-117">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="f30b3-117">Click Run.</span></span>
    * <span data-ttu-id="f30b3-118">Paleiskite ER formato konfigūracijos juodraščio versiją, norėdami generuoti Intrastat ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="f30b3-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="f30b3-119">Lauke Įveskite failo pavadinimą įveskite „intrastat.xml“.</span><span class="sxs-lookup"><span data-stu-id="f30b3-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="f30b3-120">Nurodykite failo vardą.</span><span class="sxs-lookup"><span data-stu-id="f30b3-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="f30b3-121">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="f30b3-121">Click OK.</span></span>
    * <span data-ttu-id="f30b3-122">Peržiūrėkite sugeneruotą XML failą.</span><span class="sxs-lookup"><span data-stu-id="f30b3-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="f30b3-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f30b3-123">Close the page.</span></span>
8. <span data-ttu-id="f30b3-124">Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="f30b3-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="f30b3-125">Atidarykite šią formą, kad peržiūrėtumėte Intrastat operacijas, kurios yra įtrauktos sugeneruotą elektroninį dokumentą.</span><span class="sxs-lookup"><span data-stu-id="f30b3-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="f30b3-126">Spustelėkite Intrastat archyvas.</span><span class="sxs-lookup"><span data-stu-id="f30b3-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="f30b3-127">Kadangi įvykdytame ER formate nėra jokių programos duomenų atnaujinimo parametrų, informacija apie užpildytą Intrastat ataskaitą nesuarchyvuota.</span><span class="sxs-lookup"><span data-stu-id="f30b3-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="f30b3-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f30b3-128">Close the page.</span></span>
11. <span data-ttu-id="f30b3-129">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f30b3-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]