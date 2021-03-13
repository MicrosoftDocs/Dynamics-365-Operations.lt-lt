---
title: Dokumentų numeravimas ir kuponų chronologija
description: Šioje temoje paaiškinta, kaip nustatyti ir naudoti chronologinius numerius taikomiems dokumentams ir susijusiems kuponams.
author: ikond
manager: AnnBe
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceGroup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 401195
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-15
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 31745632de7339d167ac9f18f02e6611e1a78b28
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104417"
---
# <a name="numbering-documents-and-vouchers-chronologically"></a><span data-ttu-id="045fb-103">Dokumentų numeravimas ir kuponų chronologija</span><span class="sxs-lookup"><span data-stu-id="045fb-103">Numbering documents and vouchers chronologically</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="045fb-104">Kai kuriose šalyse galioja teisiniai reikalavimai numeruoti dokumentus ir susijusius kuponus chronologine tvarka.</span><span class="sxs-lookup"><span data-stu-id="045fb-104">In some countries, there is a legal requirement to number documents and related vouchers in chronological order.</span></span> <span data-ttu-id="045fb-105">Chronologiją turi palaikyti laikotarpiai.</span><span class="sxs-lookup"><span data-stu-id="045fb-105">The chronology must be supported by periods.</span></span> <span data-ttu-id="045fb-106">Visi skaičiai, priklausantys ankstesniems laikotarpiams turi būti mažesni nei skaičiai priklausantys vėlesniems.</span><span class="sxs-lookup"><span data-stu-id="045fb-106">All of the numbers that belong to earlier periods must be less than the numbers that belong to later periods.</span></span> <span data-ttu-id="045fb-107">Norėdami atitikti šį reikalavimą, buvo įdiegta chronologinių numerių funkcija.</span><span class="sxs-lookup"><span data-stu-id="045fb-107">To meet this requirement, chronological numbering functionality has been implemented.</span></span> <span data-ttu-id="045fb-108">Šioje temoje paaiškinta, kaip konfigūruoti ir naudoti chronologinius numerius taikomiems dokumentams ir susijusiems kuponams.</span><span class="sxs-lookup"><span data-stu-id="045fb-108">This topic explains how to configure and use chronological numbers for applicable documents and related vouchers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="045fb-109">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="045fb-109">Prerequisites</span></span>

<span data-ttu-id="045fb-110">Funkcijos valdymo darbo srityje įjunkite **Chronologinio numeravimo** funkciją.</span><span class="sxs-lookup"><span data-stu-id="045fb-110">In the Feature management workspace, turn on the **Chronological numbering** feature.</span></span> <span data-ttu-id="045fb-111">Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="045fb-111">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

## <a name="configure-chronological-numbering"></a><span data-ttu-id="045fb-112">Konfigūruokite chronologinį numeravimą</span><span class="sxs-lookup"><span data-stu-id="045fb-112">Configure chronological numbering</span></span>

<span data-ttu-id="045fb-113">Chronologiniai numeravimai paveikia tolesnius dokumentus.</span><span class="sxs-lookup"><span data-stu-id="045fb-113">Chronological numbering affects the following documents.</span></span>

<span data-ttu-id="045fb-114">**Gautinos sumos**</span><span class="sxs-lookup"><span data-stu-id="045fb-114">**Accounts receivable**</span></span>
- <span data-ttu-id="045fb-115">Kliento SF</span><span class="sxs-lookup"><span data-stu-id="045fb-115">Customer invoice</span></span>
- <span data-ttu-id="045fb-116">Kliento SF kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-116">Customer invoice voucher</span></span>
- <span data-ttu-id="045fb-117">Pardavimo kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="045fb-117">Sales credit note</span></span>
- <span data-ttu-id="045fb-118">Pardavimo kredito pažymos kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-118">Sales credit note voucher</span></span>
- <span data-ttu-id="045fb-119">Laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="045fb-119">Free text invoice</span></span>
- <span data-ttu-id="045fb-120">Laisvos formos SF kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-120">Free text invoice voucher</span></span>
- <span data-ttu-id="045fb-121">Laisvos formos kredito pažyma</span><span class="sxs-lookup"><span data-stu-id="045fb-121">Free text credit note</span></span>
- <span data-ttu-id="045fb-122">Laisvos formos kredito pažymos kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-122">Free text credit note voucher</span></span>
- <span data-ttu-id="045fb-123">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="045fb-123">Packing slip</span></span>
- <span data-ttu-id="045fb-124">Važtaraščio kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-124">Packing slip voucher</span></span>
- <span data-ttu-id="045fb-125">Važtaraščio pataisos kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-125">Packing slip correction voucher</span></span>
- <span data-ttu-id="045fb-126">Delspinigių pažymos kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-126">Interest note voucher</span></span>
- <span data-ttu-id="045fb-127">Priminimo laiško kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-127">Collection letter voucher</span></span>

<span data-ttu-id="045fb-128">**Mokėtinos sumos**</span><span class="sxs-lookup"><span data-stu-id="045fb-128">**Accounts payable**</span></span>
- <span data-ttu-id="045fb-129">SF kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-129">Invoice voucher</span></span>
- <span data-ttu-id="045fb-130">Kredito pažymos kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-130">Credit note voucher</span></span>
- <span data-ttu-id="045fb-131">Gavimo dokumento kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-131">Product receipt voucher</span></span>

<span data-ttu-id="045fb-132">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="045fb-132">**Project management**</span></span>
- <span data-ttu-id="045fb-133">PVM sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="045fb-133">Invoice</span></span>
- <span data-ttu-id="045fb-134">SF kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-134">Invoice voucher</span></span>
- <span data-ttu-id="045fb-135">Kredito sąskaita</span><span class="sxs-lookup"><span data-stu-id="045fb-135">Credit note</span></span>
- <span data-ttu-id="045fb-136">Kredito pažymos kvitas</span><span class="sxs-lookup"><span data-stu-id="045fb-136">Credit note voucher</span></span> 

### <a name="define-number-sequences"></a><span data-ttu-id="045fb-137">Nustatykite skaičių sekas</span><span class="sxs-lookup"><span data-stu-id="045fb-137">Define number sequences</span></span>

<span data-ttu-id="045fb-138">Norėdami nustatyti skaičių sekas, eikite į **Organizacijos administravimas** > **Skaičių sekos** > **Skaičių sekos**.</span><span class="sxs-lookup"><span data-stu-id="045fb-138">To define number sequences, go to **Organization administration** > **Number sequences** > **Number sequences**.</span></span> <span data-ttu-id="045fb-139">Galite nustatyti tiek skaičių sekų, kiek jums reikia padengti paveiktus laikotarpius būtiniems dokumentams.</span><span class="sxs-lookup"><span data-stu-id="045fb-139">You can define as many number sequences as required to cover the affected periods for required documents.</span></span> 

<span data-ttu-id="045fb-140">Nurodykite įmonę kiekvienai skaičių sekai.</span><span class="sxs-lookup"><span data-stu-id="045fb-140">Specify a company for each number sequence.</span></span> <span data-ttu-id="045fb-141">Skaičių sekos segmentai turi būti nustatyti taip, kad pateiktų chronologinę laikotarpių tvarką.</span><span class="sxs-lookup"><span data-stu-id="045fb-141">The segments of the number sequences must be defined so that they provide chronological order for periods.</span></span> <span data-ttu-id="045fb-142">Pavyzdžiui, segmento pavadinimai gali apimti specialius priešdėlius, kurie nurodo konkretų laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="045fb-142">For example, the segment names can contain a special prefix that identifies a specific period.</span></span>

![Skaičių sekos nustatymai](media/chrono-num-sequence.jpg)

### <a name="configure-number-sequence-groups"></a><span data-ttu-id="045fb-144">Konfigūruoti skaičių sekos grupes</span><span class="sxs-lookup"><span data-stu-id="045fb-144">Configure number sequence groups</span></span>

<span data-ttu-id="045fb-145">Norėdami konfigūruoti skaičių sekos grupes, eikite į **Gautinos sąskaitos** > **Nustatymai** > **Gautinų sąskaitaų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="045fb-145">To configure number sequence groups, go to **Accounts receivable** > **Setup** > **Accounts receivable parameters**.</span></span> <span data-ttu-id="045fb-146">Skirtuke **Skaičių sekos** nustatykite tiek skaičių grupių, kiek jums reikia padengti paveiktų laikotarpių.</span><span class="sxs-lookup"><span data-stu-id="045fb-146">On the **Number sequences** tab, define as many number sequences groups as required to cover the affected periods.</span></span> 

<span data-ttu-id="045fb-147">Kiekvienai grupei **Nuorodos** skyriuje pasirinkite vieną palaikomą dokumento nuorodą ir **Skaičių sekos kodas** laukelyje nurodykite į skaičių seką, kuri anksčiau buvo sukurta susijusiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="045fb-147">For each group, in the **Reference** section, select one of the supported document references, and in the **Number sequence code** field, refer to a number sequence that was previously created for the related period.</span></span>

![Numeravimo grupės nustatymas](media/chrono-num-sequence-group.jpg)

<span data-ttu-id="045fb-149">Panašiai, konfigūruokite skaičių sekų grupes **Mokėtinos sąskaitos** ir **Projekto valdymas ir apskaitos** moduliai.</span><span class="sxs-lookup"><span data-stu-id="045fb-149">Similarly, configure number sequence groups in **Accounts payable** and **Project management and accounting** modules.</span></span>

### <a name="configure-number-sequence-groups-chronology"></a><span data-ttu-id="045fb-150">Konfigūruoti skaičių sekos grupių chronologija</span><span class="sxs-lookup"><span data-stu-id="045fb-150">Configure number sequence groups chronology</span></span>

<span data-ttu-id="045fb-151">Norėdami konfigūruoti sekos grupių chronologiją, eikite į **Organizacijos administravimas** > **Skaičių sekos** > **Chronologinės skaičių sekos grupės**.</span><span class="sxs-lookup"><span data-stu-id="045fb-151">To configure number sequence groups chronology, go to **Organization administration** > **Number sequences** > **Chronological number sequence groups**.</span></span> <span data-ttu-id="045fb-152">Nustatykite taikomas sąlygas skaičių sekos grupėms.</span><span class="sxs-lookup"><span data-stu-id="045fb-152">Define the applicability conditions for number sequence groups.</span></span>

![Chronologinių skaičių nustatymas](media/chrono-num-sequence-group-period.jpg)

| <span data-ttu-id="045fb-154">Laukas</span><span class="sxs-lookup"><span data-stu-id="045fb-154">Field</span></span>            | <span data-ttu-id="045fb-155">aprašymas</span><span class="sxs-lookup"><span data-stu-id="045fb-155">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="045fb-156">Galioja</span><span class="sxs-lookup"><span data-stu-id="045fb-156">Effective</span></span>  | <span data-ttu-id="045fb-157">Skaičių sekos grupės taikomumo pradžios data.</span><span class="sxs-lookup"><span data-stu-id="045fb-157">The start date of number sequence group applicability.</span></span> |
| <span data-ttu-id="045fb-158">Galiojimas</span><span class="sxs-lookup"><span data-stu-id="045fb-158">Expiration</span></span>      | <span data-ttu-id="045fb-159">Skaičių sekos grupės taikomumo pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="045fb-159">The end date of number sequence group applicability.</span></span> <span data-ttu-id="045fb-160">Jei netaikoma pabaigos data, pasirinkite **Niekada**.</span><span class="sxs-lookup"><span data-stu-id="045fb-160">If no end date is applied, select **Never**.</span></span> |
| <span data-ttu-id="045fb-161">Numeracijų grupė</span><span class="sxs-lookup"><span data-stu-id="045fb-161">Number sequence group</span></span> | <span data-ttu-id="045fb-162">Skaičių sekos grupė, kuri bus naudojama siekiant sukurti dokumentų skaičius laikotarpio metu.</span><span class="sxs-lookup"><span data-stu-id="045fb-162">Number sequence group that will be used to generate document numbers during the period.</span></span> |
| <span data-ttu-id="045fb-163">Pradinė numerių sekų grupė</span><span class="sxs-lookup"><span data-stu-id="045fb-163">Original number sequence group</span></span> | <span data-ttu-id="045fb-164">Šis skaičiaus sekos grupės kodas yra naudojamas papildomiems filtrams atvejais, kai dokumentai jau turi konkrečią priskirtą *nuolatinį* skaičiaus sekos grupę.</span><span class="sxs-lookup"><span data-stu-id="045fb-164">This number sequence group code is used for additional filtering for the cases when documents already have a specific *permanent* number sequence group assigned.</span></span> <span data-ttu-id="045fb-165">Tuščia vertė yra laikoma konkrečia verte.</span><span class="sxs-lookup"><span data-stu-id="045fb-165">An empty value is considered a specific value.</span></span> <span data-ttu-id="045fb-166">Jei jums reikia ignoruoti preliminariai priskirtą grupę, naudokite **Nustatytąją** parinktį šiam nustatymui.</span><span class="sxs-lookup"><span data-stu-id="045fb-166">If you need to ignore a preliminary assigned group, use the **Default** option for this setup.</span></span> |
| <span data-ttu-id="045fb-167">Numatyta</span><span class="sxs-lookup"><span data-stu-id="045fb-167">Default</span></span> | <span data-ttu-id="045fb-168">Jei įjungta, sistema ignoruos preliminariai paskirtą dokumento numerių skaičiaus grupę ir naudos tik laikotarpių pradžios ir pabaigos datas taikomumo analizei.</span><span class="sxs-lookup"><span data-stu-id="045fb-168">If turned on, the system ignores the preliminary assigned document number sequence group and uses only the periods start and end dates for applicability analysis.</span></span> <span data-ttu-id="045fb-169">Jei išjungta, sistema naudos visą kombinaciją **Galiojantis** + **Pabaigos** + **Originali skaičių sekos grupė** pasirinkimui.</span><span class="sxs-lookup"><span data-stu-id="045fb-169">If turned off, the system uses the full combination **Effective** + **Expiration** + **Original number sequence group** for selection.</span></span> |

## <a name="document-posting"></a><span data-ttu-id="045fb-170">Dokumento publikavimas</span><span class="sxs-lookup"><span data-stu-id="045fb-170">Document posting</span></span>
<span data-ttu-id="045fb-171">Jums publikuojant dokumentą, atitinkama skaičių sekos grupė yra priskirta dokumentai pagal jo publikavimo datą ir tuomet naudojama siekiant sukurti dokumento numerį pagal aptiktą skaičių seką.</span><span class="sxs-lookup"><span data-stu-id="045fb-171">When you post a document, the appropriate number sequence group is assigned to the document, based on document's posting date, and then used to generate a document number based on the detected number sequence.</span></span> <span data-ttu-id="045fb-172">Sistema pateikia pranešimą dėl skaičiaus sekos grupės priskyrimo.</span><span class="sxs-lookup"><span data-stu-id="045fb-172">The system provides a message regarding the number sequence group assignment.</span></span>

![Dokumento numeris](media/chrono-num-sequence-fti.jpg)

> [!NOTE]
> <span data-ttu-id="045fb-174">Kai kuriose šalyse yra konkreti jau dokumento numeravimui taikoma logika.</span><span class="sxs-lookup"><span data-stu-id="045fb-174">For some countries, there is a specific logic already implemented for document numbering.</span></span> <span data-ttu-id="045fb-175">Tokiu atveju, šaliai galiojanti konkreti logika viršys **Chronologinio numeravimo** funkciją.</span><span class="sxs-lookup"><span data-stu-id="045fb-175">In this case, country-specific logic will override the **Chronological numbering** feature.</span></span>
