---
title: "Sugeneruotų failų skaidymas pagal failo dydį ir turinio kiekį"
description: "Šioje temoje pateikta informacija apie tai, kaip skaidyti sugeneruotus failus pagal failo dydį ir turinio elementų kiekį."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: afdf5b2596af7641182be50ced8159967164b115
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="d300f-103">Sugeneruotų XML failų skaidymas pagal failo dydį ir turinio kiekį</span><span class="sxs-lookup"><span data-stu-id="d300f-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d300f-104">Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus generuoti siunčiamus dokumentus XLS formatu.</span><span class="sxs-lookup"><span data-stu-id="d300f-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="d300f-105">Kartais šie dokumentai gali būti priimti tik tada, kai atitinka konkrečius kriterijus, pvz., maksimalus failo dydis arba didžiausias kai kurių XML mazgų skaičius.</span><span class="sxs-lookup"><span data-stu-id="d300f-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="d300f-106">Galite kurti ER formatus, skirtus generuoti elektroninius dokumentus, kurie atitiktų šių dokumentų gavėjų nurodytus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="d300f-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="d300f-107">FAILO formato elementui, galite nustatyti failo dydžio ribą kaip ER išraišką.</span><span class="sxs-lookup"><span data-stu-id="d300f-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="d300f-108">Viršijus nustatytą ribą generuojant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.</span><span class="sxs-lookup"><span data-stu-id="d300f-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="d300f-109">Bet kuriam formatui XML ELEMENTAS galite nustatyti elementų skaičiaus ribą kaip ER išraišką.</span><span class="sxs-lookup"><span data-stu-id="d300f-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="d300f-110">Sugeneruotame faile viršijus nustatytą XML mazgų ribą vykdant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.</span><span class="sxs-lookup"><span data-stu-id="d300f-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="d300f-111">Bet kuriam formato XML SEKA elementui galite nustatyti antrinių elementų skaičiaus ribą kaip ER išraišką.</span><span class="sxs-lookup"><span data-stu-id="d300f-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="d300f-112">Sugeneruotame faile viršijus nustatytą formato elemento įdėtųjų XML mazgų ribą vykdant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.</span><span class="sxs-lookup"><span data-stu-id="d300f-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="d300f-113">Galite pažymėti bet kurį XML ELEMENTAS formato elementą kaip neperkeliamąjį.</span><span class="sxs-lookup"><span data-stu-id="d300f-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="d300f-114">Tokiu būdu galite išlaikyti įdėtuosius XML mazgų elementus, sugeneruotus pagal formato elementą, viename sugeneruotame faile.</span><span class="sxs-lookup"><span data-stu-id="d300f-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="d300f-115">Be to, be formato elementų XML ELEMENTAS ir XML SEKA, XML mazgams įtraukti į sugeneruotą failą galite naudoti formato elementą NEAPDOROTAS XML.</span><span class="sxs-lookup"><span data-stu-id="d300f-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="d300f-116">Tačiau mazgų, kuriuos įtrauksite naudodami formato elementą NEAPDOROTAS XML, nėra paisoma skaičiuojant mazgus, siekiant įvertinti elementų skaičiaus ribas.</span><span class="sxs-lookup"><span data-stu-id="d300f-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="d300f-117">Jei sukonfigūravote formato elemento FAILAS failų paskirties vietas, kuris sukonfigūruotas skaidyti sugeneruotą išvestį, kai viršijamos konkrečios ribos, kiekviena sugeneruotos išvesties dalis siunčiama į sukonfigūruotą failo paskirties vietą kaip atskiras failas.</span><span class="sxs-lookup"><span data-stu-id="d300f-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="d300f-118">Norėdami unikaliai pavadinti failus, kurie sukuriami suskaidžius išvestį, turite sukonfigūruoti formato elemento FAILAS ER išraišką.</span><span class="sxs-lookup"><span data-stu-id="d300f-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="d300f-119">Jei norite įtraukti NUMERACIJA tipo ER duomenų šaltinį, numeracija bus didinama su kiekviena suskaidytos išvesties dalimi.</span><span class="sxs-lookup"><span data-stu-id="d300f-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="d300f-120">Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlį **ER XML failai, suskaidyti atsižvelgiant į failo dydį arba turinio elementų kiekį**, kuris yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** verslo proceso dalis ir gali būti atsisiųstas iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="d300f-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="d300f-121">Šis užduočių vedlys padės ER formato konfigūravimo proceso metu, norint skaidyti sugeneruotus failus atsižvelgiant į failo dydžio ir turinio elementų kiekio ribas.</span><span class="sxs-lookup"><span data-stu-id="d300f-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="d300f-122">Norėdami užbaigti užduočių vedlį, turite atsisiųsti šiuos failus:</span><span class="sxs-lookup"><span data-stu-id="d300f-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="d300f-123">ER modelio konfigūracija – XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="d300f-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="d300f-124">ER formato konfigūracija – XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="d300f-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="d300f-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d300f-125">Additional resources</span></span>
[<span data-ttu-id="d300f-126">Elektroninių ataskaitų paskirties vietos</span><span class="sxs-lookup"><span data-stu-id="d300f-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="d300f-127">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="d300f-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)


