---
title: Numerio lentelės etikečių dokumentų maršrutų planavimo maketas
description: Šioje temoje aprašoma, kaip naudoti formatavimo metodus spausdinti reikšmėms etiketėse.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 8c96aef5d66ed8f8c44d74eee9b60f0a7d38a46d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017718"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="cde38-103">Numerio lentelės etikečių dokumentų maršrutų planavimo maketas</span><span class="sxs-lookup"><span data-stu-id="cde38-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cde38-104">Dokumento maršruto planavimo maketas apibrėžia numerio lentelės etikečių maketą ir ant etikečių išspausdintus duomenis.</span><span class="sxs-lookup"><span data-stu-id="cde38-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="cde38-105">Spausdinimo aktyvinimo taškus galite konfigūruoti, kai nustatote mobiliojo įrenginio meniu elementus ir darbo šablonus.</span><span class="sxs-lookup"><span data-stu-id="cde38-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="cde38-106">Paprastai sandėlio gavimo klerkai spausdina numerio lentelės etiketes iš karto po to, kai įrašo padėklų, kurie pristatomi į gavimo sritį, turinį.</span><span class="sxs-lookup"><span data-stu-id="cde38-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="cde38-107">Fizinės etiketės pritaikomos padėklams.</span><span class="sxs-lookup"><span data-stu-id="cde38-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="cde38-108">Jos gali būti naudojamos tolesnei atidėjimo proceso tikrinimo daliai ir būsimoms siuntimo paėmimo operacijoms.</span><span class="sxs-lookup"><span data-stu-id="cde38-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="cde38-109">Galite spausdinti itin sudėtingas etiketes, jei spausdinimo įrenginys gali suprasti jam siunčiamą tekstą.</span><span class="sxs-lookup"><span data-stu-id="cde38-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="cde38-110">Pavyzdžiui, „Zebra” programavimo kalbos (ZPL) maketas, kuriame yra brūkšninis kodas, gali būti panašus į toliau pateiktą pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="cde38-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="cde38-111">Etikečių spausdinimo proceso metu tekstas, , šiame pavyzdyje – `$LicensePlateId$`, bus pakeistas į duomenų reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cde38-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="cde38-112">Norėdami pamatyti reikšmes, kurios bus išspausdintos, eikite į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Numerio lentelės etiketės**.</span><span class="sxs-lookup"><span data-stu-id="cde38-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="cde38-113">Keletas plačiai prieinamų etikečių generavimo įrankių gali padėti formatuoti etiketės maketo tekstą.</span><span class="sxs-lookup"><span data-stu-id="cde38-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="cde38-114">Dauguma šių įrankių palaiko `$FieldName$` formatą.</span><span class="sxs-lookup"><span data-stu-id="cde38-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="cde38-115">Be to, „Microsoft Dynamics 365 Supply Chain Management” naudoja specialią formatavimo logiką, kuri yra dokumento maršruto planavimo maketo laukų susiejimo dalis.</span><span class="sxs-lookup"><span data-stu-id="cde38-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="cde38-116">Pasirinktiniai numerių formatai</span><span class="sxs-lookup"><span data-stu-id="cde38-116">Custom number formats</span></span>

<span data-ttu-id="cde38-117">Galite tinkinti skaitinių lauko reikšmių, kurios spausdinamos naudojant kodus, turinčius toliau pateikiamą formatą, formatavimą.</span><span class="sxs-lookup"><span data-stu-id="cde38-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="cde38-118">Toliau pateikiamas šio formato paaiškinimas.</span><span class="sxs-lookup"><span data-stu-id="cde38-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="cde38-119">`FieldName` yra duomenų lauko pavadinimas (pvz., **Kiekis** ).</span><span class="sxs-lookup"><span data-stu-id="cde38-119">`FieldName` is the name of the data field (such as **Qty** ).</span></span>
- <span data-ttu-id="cde38-120">`FormatString` nurodo, kaip turi būti spausdinami duomenys.</span><span class="sxs-lookup"><span data-stu-id="cde38-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="cde38-121">Toliau pateikti pavyzdžiai rodo, kaip galima tinkinti darbo kiekio ( **Kiekis** ) lauką.</span><span class="sxs-lookup"><span data-stu-id="cde38-121">The following examples show how you can customize the work quantity ( **Qty** ) field:</span></span>

- <span data-ttu-id="cde38-122">Naudokite `$Qty:0000$`, norėdami visada matyti keturis skaitmenis (nuliai naudojami kaip vietos rezervavimo ženklai).</span><span class="sxs-lookup"><span data-stu-id="cde38-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="cde38-123">Pavyzdžiui, jei kiekis yra 10, etiketėje bus rodoma „0010”.</span><span class="sxs-lookup"><span data-stu-id="cde38-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="cde38-124">Naudokite `$Qty:0.00$`, norėdami visada matyti du skaičius po kablelio.</span><span class="sxs-lookup"><span data-stu-id="cde38-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="cde38-125">Pavyzdžiui, jei kiekis yra 10, etiketėje bus rodoma „10.00”.</span><span class="sxs-lookup"><span data-stu-id="cde38-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="cde38-126">Norėdami peržiūrėti visą galimų numerių formato eilučių sąrašą, žr. [Pasirinktinės skaitinės formato eilutės](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="cde38-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="cde38-127">Pasirinktiniai eilučių formatai</span><span class="sxs-lookup"><span data-stu-id="cde38-127">Custom string formats</span></span>

<span data-ttu-id="cde38-128">Galite pašalinti pirmuosius eilutės simbolius naudodami toliau pateiktą lauką ir formato kodą.</span><span class="sxs-lookup"><span data-stu-id="cde38-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="cde38-129">`#` nurodo praleidžiamų simbolių skaičių.</span><span class="sxs-lookup"><span data-stu-id="cde38-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="cde38-130">Pavyzdžiui, norėdami išspausdinti gabenimo konteinerio serijos kodo (SSCC) numerio lentelės numerį, kuris neapima pirmų dviejų simbolių, naudokite `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="cde38-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="cde38-131">Šiuo atveju numerio lentelės numeris „0011111111111222221” bus išspausdintas kaip „11111111111222221”.</span><span class="sxs-lookup"><span data-stu-id="cde38-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="cde38-132">Pasirinktiniai datos / laiko formatai</span><span class="sxs-lookup"><span data-stu-id="cde38-132">Custom date/time formats</span></span>

<span data-ttu-id="cde38-133">Toliau pateiktame pavyzdyje parodyta, kaip galima kontroliuoti formatą, kuris naudojamas datoms spausdinti.</span><span class="sxs-lookup"><span data-stu-id="cde38-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="cde38-134">Šiame pavyzdyje data 2020 m. balandžio 30 d. bus spausdinama kaip „30-04-2020”.</span><span class="sxs-lookup"><span data-stu-id="cde38-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="cde38-135">Norėdami peržiūrėti visą galimų datos / laiko formatų sąrašą, žr. [Pasirinktinės datos ir laiko formato eilutės](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="cde38-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="cde38-136">Kelių eilučių duomenų atskirų eilučių spausdinimas</span><span class="sxs-lookup"><span data-stu-id="cde38-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="cde38-137">Jei duomenų lauke yra kelios eilutės (t. y. eilutės, kurios yra atskirtos eilučių lūžiais), galite spausdinti atskirą eilutę naudodami toliau pateiktą formatą.</span><span class="sxs-lookup"><span data-stu-id="cde38-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="cde38-138">`#` yra eilutės numeris, kurį norite spausdinti.</span><span class="sxs-lookup"><span data-stu-id="cde38-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="cde38-139">(Pirmai eilutei naudokite 1.)</span><span class="sxs-lookup"><span data-stu-id="cde38-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="cde38-140">Pavyzdžiui, jūsų sistemoje yra `AdditionalAddress` laukas, kuriame saugomas toliau pateiktas kelių eilučių adresas.</span><span class="sxs-lookup"><span data-stu-id="cde38-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="cde38-141">„Contoso Inc.”</span><span class="sxs-lookup"><span data-stu-id="cde38-141">Contoso Inc.</span></span>  
<span data-ttu-id="cde38-142">Gatvės pavadinimas 123</span><span class="sxs-lookup"><span data-stu-id="cde38-142">123 Street Name</span></span>  
<span data-ttu-id="cde38-143">Miestas, Valstija</span><span class="sxs-lookup"><span data-stu-id="cde38-143">Some City, Some State</span></span>

<span data-ttu-id="cde38-144">Galite spausdinti šį adresą po vieną eilutę, naudodami toliau pateiktus kodus.</span><span class="sxs-lookup"><span data-stu-id="cde38-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="cde38-145">Kodas</span><span class="sxs-lookup"><span data-stu-id="cde38-145">Code</span></span> | <span data-ttu-id="cde38-146">Išspausdintas tekstas</span><span class="sxs-lookup"><span data-stu-id="cde38-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="cde38-147">„Contoso Inc.”</span><span class="sxs-lookup"><span data-stu-id="cde38-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="cde38-148">Gatvės pavadinimas 123</span><span class="sxs-lookup"><span data-stu-id="cde38-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="cde38-149">Miestas, Valstija</span><span class="sxs-lookup"><span data-stu-id="cde38-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="cde38-150">Spausdinimas ir formatavimas naudojant rodymo būdą</span><span class="sxs-lookup"><span data-stu-id="cde38-150">Print and format from a display method</span></span>

<span data-ttu-id="cde38-151">Galite spausdinti iš rodymo būdo naudodami toliau pateiktą formatą.</span><span class="sxs-lookup"><span data-stu-id="cde38-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="cde38-152">Šį formatą galite derinti su kitais šioje temoje aprašytais tipais.</span><span class="sxs-lookup"><span data-stu-id="cde38-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="cde38-153">Pavyzdžiui, turite rodymo būdą, kurio pavadinimas `DisplayListOfItemsNumbers()`, ir norite spausdinti pirmą šio būdo prekės numerį.</span><span class="sxs-lookup"><span data-stu-id="cde38-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="cde38-154">Tokiu atveju galite naudoti toliau pateiktą kodą.</span><span class="sxs-lookup"><span data-stu-id="cde38-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="cde38-155">Daugiau informacijos apie tai, kaip spausdinti etiketes</span><span class="sxs-lookup"><span data-stu-id="cde38-155">More information about how to print labels</span></span>

<span data-ttu-id="cde38-156">Daugiau informacijos apie tai, kaip nustatyti ir spausdinti etiketes, žr. [Numerio lentelės etiketės spausdinimo įgalinimas](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="cde38-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>
