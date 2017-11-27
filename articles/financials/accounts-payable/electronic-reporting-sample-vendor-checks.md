---
title: "Elektroninės ataskaitos tiekėjo čekių pavyzdžiai"
description: "Šioje temoje pateikiama bendra informacija apie tai, kaip naudoti elektroninės ataskaitos čekių formatų pavyzdžius."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c9abea228cdaae84ca2b9aada9f36bbe79c1dc6b
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="033d8-103">Elektroninės ataskaitos čekių formatų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="033d8-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="033d8-104">Norėdami formatuoti tiekėjo čekius, galite naudoti elektronines ataskaitas (ER).</span><span class="sxs-lookup"><span data-stu-id="033d8-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="033d8-105">Rinkoje siūloma daug bankui skirtų ir čekio tiekėjui skirtų čekio formatų.</span><span class="sxs-lookup"><span data-stu-id="033d8-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="033d8-106">Čekių formatų pavyzdžiai įtraukti į elektroninių ataskaitų rengimo įrankio saugyklos mokėjimo čekio modelį.</span><span class="sxs-lookup"><span data-stu-id="033d8-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="033d8-107">Šie čekių pavyzdžiai pažymėti **Tikrinti viduryje (JAV)** ir **Tikrinti žemiau pateiktoje viršutinėje šaknelėje (JAV)**.</span><span class="sxs-lookup"><span data-stu-id="033d8-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="033d8-108">Kokie čekio formatai šiuo metu palaikomi?</span><span class="sxs-lookup"><span data-stu-id="033d8-108">What check formats are currently supported?</span></span>

<span data-ttu-id="033d8-109">Visada turite eiti į bendrai naudojamo turto biblioteką „Microsoft Dynamics“ skirtą „Lifecycle Services“ (LCS) ir peržiūrėti dabartinį prieinamų failų, kurių turto tipas yra **GER konfigūracija**, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="033d8-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="033d8-110">Kitame skyriuje – „Ką turiu nustatyti?“ – pateikiama nuoroda į temą, kurioje paaiškinta, kaip sukurti LCS saugyklą, kad galėtumėte peržiūrėti galimas konfigūracijas ir importuoti pasirinktas konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="033d8-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="033d8-111">„Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidime pateikiamas formato, kai čekis yra viršuje ir po jo eina dvi pavedimo dalys, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="033d8-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="033d8-112">Taip pat pateikiamas formato, kai čekis yra viduryje, tarp dviejų pavedimo dalių, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="033d8-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="033d8-113">Šių formatų pavyzdžiai atitinka „Deluxe“ verslo čekių formatus.</span><span class="sxs-lookup"><span data-stu-id="033d8-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="033d8-114">Ką turiu nustatyti?</span><span class="sxs-lookup"><span data-stu-id="033d8-114">What do I have to set up?</span></span>

- <span data-ttu-id="033d8-115">Prieš spausdinant čekius naudojant ER (elektronines ataskaitas) į ER (elektroninių ataskaitų) konfigūracijas būtina importuoti bent vieną aktyvią čekio konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="033d8-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="033d8-116">Instrukcijų ieškokite [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="033d8-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="033d8-117">Kai konfigūruojate banko sąskaitos grynųjų pinigų ir banko valdymo čekius, pažymėkite žymės langelį **Bendrasis eksporto elektroniniu būdu formatas**, o po to pasirinkite atitinkamą čekio formatą kaip eksportavimo formato konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="033d8-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="033d8-118">Taip pat turite nurodyti pavedime spausdinamų važtaraščio eilučių skaičių.</span><span class="sxs-lookup"><span data-stu-id="033d8-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="033d8-119">Skaičiuodami šį skaičių būtinai įtraukite antraštės eilutes.</span><span class="sxs-lookup"><span data-stu-id="033d8-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="033d8-120">Rekomenduojamas šių dviejų čekio formatų pavyzdžių kvito eilučių skaičius yra 17.</span><span class="sxs-lookup"><span data-stu-id="033d8-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="033d8-121">Tačiau, atsižvelgiant į jūsų čekius ir jūsų spausdintuvo tvarkykles, šis skaičius skirsis.</span><span class="sxs-lookup"><span data-stu-id="033d8-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="033d8-122">Mes rekomenduojame atsispausdinti bandomąjį čekį ir patikrinti čekio maketą.</span><span class="sxs-lookup"><span data-stu-id="033d8-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="033d8-123">Norėdami atsispausdinti bandomąjį čekį, pažymėkite parinktį **Bandomasis spausdinimas**.</span><span class="sxs-lookup"><span data-stu-id="033d8-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="033d8-124">Čekio formatų pavyzdžius geriausiai naudoti tada, kai nustatyta išplėstinių „Microsoft Excel“ spausdintuvo ypatybių dalies **Paraštės** parinktis **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="033d8-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="033d8-125">Sugeneravę bandomąjį čekį įjunkite „Excel“ išvesties redagavimą ir sukonfigūruokite puslapio išdėstymą taip, kad būtų nustatyta visų paraščių parinktis **0** (nulis).</span><span class="sxs-lookup"><span data-stu-id="033d8-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="033d8-126">Palyginkite bandomąją čekių kopiją su jūsų turimais čekiais ir koreguokite parametrus tol, kol nustatysite norimą lygiuotę.</span><span class="sxs-lookup"><span data-stu-id="033d8-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="033d8-127">Kai mokėjimo žurnale generuojate sukonfigūruotos banko sąskaitos mokėjimus, čekiai bus spausdinami naudojant nurodytą formatą.</span><span class="sxs-lookup"><span data-stu-id="033d8-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="033d8-128">Daugiau informacijos rasite [Elektroninių ataskaitų formato modifikavimas](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md)).</span><span class="sxs-lookup"><span data-stu-id="033d8-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

