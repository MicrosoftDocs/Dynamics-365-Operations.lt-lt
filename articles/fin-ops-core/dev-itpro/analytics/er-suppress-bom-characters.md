---
title: ER konfigūracijų kūrimas tam, kad sugeneruotuose failuose nebūtų rodomi KS simboliai
description: Šioje temoje paaiškinama, kaip konfigūruoti elektroninių ataskaitų (ER) formatą generuoti ataskaitoms, nerodančioms baitų eiliškumo žymos (KS) simbolių.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fabc308b1b0682c6fdce3e81e7335417846bebd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743538"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="bf40f-103">ER konfigūracijų kūrimas tam, kad sugeneruotuose failuose nebūtų rodomi KS simboliai</span><span class="sxs-lookup"><span data-stu-id="bf40f-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf40f-104">Galite sukurti [Elektroninių ataskaitų (ER)](general-electronic-reporting.md) [sprendimą](er-quick-start1-new-solution.md) siunčiamų dokumentų generavimui.</span><span class="sxs-lookup"><span data-stu-id="bf40f-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="bf40f-105">Norint generuoti dokumentus kaip tekstinius arba XML failus, sprendimas turi apimti ER [konfigūraciją](general-electronic-reporting.md#Configuration) su ER [formato](general-electronic-reporting.md#FormatComponentOutbound) komponentu.</span><span class="sxs-lookup"><span data-stu-id="bf40f-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="bf40f-106">Norint nurodyti [simbolio kodavimą](https://docs.microsoft.com/windows/win32/intl/character-sets), atitinkantį simbolių rinkinį sugeneruotuose failuose, ER formate turi būti **Bendra\\Failas** formato elementas.</span><span class="sxs-lookup"><span data-stu-id="bf40f-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="bf40f-107">Norėdami konfigūruoti ER formato komponentą, atidarykite ER konfigūracijos [juodraščio](general-electronic-reporting.md#component-versioning) versiją ER formato dizaino įrankyje ir pridėkite **Bendra\\Failas** elementą.</span><span class="sxs-lookup"><span data-stu-id="bf40f-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="bf40f-108">Lauke **Kodavimas** nurodykite siunčiamų failų, kurios generuojami vykdymo aplinkoje naudojant šį komponentą, kodavimą.</span><span class="sxs-lookup"><span data-stu-id="bf40f-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="bf40f-109">Jei formate yra neteisingas kodavimo pavadinimas, įrašant formato parametrų pakeitimus įvyksta klaida.</span><span class="sxs-lookup"><span data-stu-id="bf40f-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Šakninio elemento pridėjimas Formato dizaino įrankio puslapyje](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="bf40f-111">Jei kaip kodavimą nurodysite **„UTF-8”**, **„UTF-16”** arba **„UTF-32”**, parinktis **Nerodyti KS simbolių** taps galima.</span><span class="sxs-lookup"><span data-stu-id="bf40f-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="bf40f-112">Nustatykite šią parinktį į **Taip** tam, kad [baitų eiliškumo žymos (KS) simboliai](https://docs.microsoft.com/globalization/encoding/byte-order-mark) būtų nerodomi siunčiamuose failuose, sugeneruotuose vykdymo aplinkoje, kai vykdomas redaguotinas ER formatas.</span><span class="sxs-lookup"><span data-stu-id="bf40f-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="bf40f-113">Jei paliksite lauką **Kodavimas** tuščią, bus naudojamas numatytasis **„UTF-8”** kodavimas.</span><span class="sxs-lookup"><span data-stu-id="bf40f-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Parinkties Nerodyti KS simbolių nustatymas Formato dizaino įrankio puslapyje](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="bf40f-115">Norėdami peržiūrėti funkciją vykdymo aplinkoje, atlikite atitinkamą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="bf40f-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="bf40f-116">Pavyzdžiui, atlikite temos [ER formato XML elementų vykdymo atidėjimas](er-defer-xml-element.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bf40f-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="bf40f-117">Atlikę šios temos skyriaus [Suvestinės XML elemento vykdymo atidėjimas apskaičiuoto bendro skaičiaus panaudojimui](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) veiksmus, atlikite šiuos papildomus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bf40f-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="bf40f-118">UTF kodavimui nurodyti:</span><span class="sxs-lookup"><span data-stu-id="bf40f-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="bf40f-119">Pasirinkite **Bendra\\Failas** tipo elementą **Ataskaita**.</span><span class="sxs-lookup"><span data-stu-id="bf40f-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="bf40f-120">Lauke **Kodavimas** nurodykite **„UTF-8”** kodavimą.</span><span class="sxs-lookup"><span data-stu-id="bf40f-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="bf40f-121">XML failo su KS simboliais generavimui:</span><span class="sxs-lookup"><span data-stu-id="bf40f-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="bf40f-122">Nustatykite parinktį **Nerodyti KS simbolių** į **Ne** tam, kad KS simboliai būtų įtraukti į sugeneruotus XML failus.</span><span class="sxs-lookup"><span data-stu-id="bf40f-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="bf40f-123">Atlikite veiksmus, nurodytus temos [ER formato XML elementų vykdymo atidėjimas](er-defer-xml-element.md) skyriuje [Suvestinės XML elemento vykdymo atidėjimas apskaičiuoto bendro skaičiaus panaudojimui](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ir įrašykite sugeneruotą failą kaip **„SampleXmlReport.xml”**.</span><span class="sxs-lookup"><span data-stu-id="bf40f-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="bf40f-124">XML failo be KS simbolių generavimui:</span><span class="sxs-lookup"><span data-stu-id="bf40f-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="bf40f-125">Nustatykite parinktį **Nerodyti KS simbolių** į **Taip** tam, kad KS simboliai būtų nerodomi sugeneruotuose XML failuose.</span><span class="sxs-lookup"><span data-stu-id="bf40f-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="bf40f-126">Atlikite veiksmus, nurodytus temos [ER formato XML elementų vykdymo atidėjimas](er-defer-xml-element.md) skyriuje [Suvestinės XML elemento vykdymo atidėjimas apskaičiuoto bendro skaičiaus panaudojimui](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) ir įrašykite sugeneruotą failą kaip **„SampleXmlReport (1).xml”**.</span><span class="sxs-lookup"><span data-stu-id="bf40f-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="bf40f-127">Failų lyginimo priemonėje palyginkite sugeneruotus failus.</span><span class="sxs-lookup"><span data-stu-id="bf40f-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="bf40f-128">Pirmas skirtumas, kurį pastebėsite, yra failo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="bf40f-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="bf40f-129">Faile „SampleXmlReport.xml” yra KS simbolis, o faile „SampleXmlReport (1).xml” – nėra.</span><span class="sxs-lookup"><span data-stu-id="bf40f-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Sugeneruotų failų palyginimas naudojant failų lyginimo priemonę](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="bf40f-131">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="bf40f-131">See also</span></span>

- [<span data-ttu-id="bf40f-132">XML elementų ER formatais vykdymo atidėjimas</span><span class="sxs-lookup"><span data-stu-id="bf40f-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]