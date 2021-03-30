---
title: Nustatyti papildomą asmenį konsolidavimo procesui
description: Šioje temoje paaiškinama, kaip dirbti su sąskaitų grafikais konsoliduojant bendroves.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 4ffe0ac0b11a3f58ca4a893d8786f04b4067b270
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975538"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a><span data-ttu-id="1a388-103">Nustatyti papildomą asmenį konsolidavimo procesui</span><span class="sxs-lookup"><span data-stu-id="1a388-103">Set up a subsidiary legal entity for consolidation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a388-104">Metodas, kurį naudojate siekiant parengti papildomas sąskaitas konsolidavimui priklauso iš dalies nuo plėtinio, prie kurio sąskaitų grafiko struktūra papildomuose juridiniuose asmenyse parodo sąskaitų grafiką konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-104">The method that you use to prepare subsidiary accounts for consolidation depends in part on the extent to which the structure of the chart of accounts in the subsidiary legal entity reflects the chart of accounts in the consolidated legal entity.</span></span>

<span data-ttu-id="1a388-105">Prieš jums pradedant konsoliduoti kaip laikotarpio pabaigos uždarymo dalį, užbaikite parengimo veiksmus ilgo laiko uždarymui, bet neuždarykite papildomų sąskaitų iki konsolidavimo pabaigos.</span><span class="sxs-lookup"><span data-stu-id="1a388-105">Before you start a consolidation as part of period-end closing, complete the preparatory activities for the period-end closing, but don't close the subsidiary accounts until the consolidation is completed.</span></span> <span data-ttu-id="1a388-106">Dėl daugiau informacijos apie ilgalaikio laikotarpio uždarymą, žr. [Uždaryti bendrą buhalterinę knygą po laikotarpio](close-general-ledger-at-period-end.md) ir [Uždaryti mokestinius metus](tasks/close-fiscal-year.md).</span><span class="sxs-lookup"><span data-stu-id="1a388-106">For more information about period-end closing, see [Close the general ledger at period end](close-general-ledger-at-period-end.md) and [Close the fiscal year](tasks/close-fiscal-year.md).</span></span>

> [!NOTE]
>  <span data-ttu-id="1a388-107">Rekomenduojame jums naudoti „Management Reporter“ „Microsoft Dynamics 365 Finance“ siekiant suderinti finansinius rezultatus keliems juridiniams asmenims konsoliduotame formate.</span><span class="sxs-lookup"><span data-stu-id="1a388-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="1a388-108">„Management Reporter“ leidžia jums kurti konsoliduotas finansines ataskaitas juridiniuose objektuose, naudoti „Exce“ siekiant importuoti konsolidavimo duomenis iš kitų šaltinių ir versti sumas į bet kokių ataskaitų valiutų skaičius be poreikio vykdyti konsolidavimo procesą „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="1a388-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a><span data-ttu-id="1a388-109">Talpinkite į žemėlapį dukterinės įmonės pagrindines sąskaitas siekiant konsoliduoti pagrindines sąskaitas</span><span class="sxs-lookup"><span data-stu-id="1a388-109">Map subsidiary main accounts to consolidated main accounts</span></span>

<span data-ttu-id="1a388-110">Jei sąskaitų grafikas dukteriniame juridiniame asmenyje neseka sąskaitų grafiko konsoliduoto juridinio asmens, galite talpinti žemėlapyje pagrindines sąskaitas dukterinėje įmonėje į pagrindines sąskaitas konsoliduotame juridiname asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-110">If the chart of accounts in the subsidiary legal entity doesn't follow the chart of accounts in the consolidated legal entity, you can map the main accounts in the subsidiary to the main accounts in the consolidated legal entity.</span></span>

1. <span data-ttu-id="1a388-111">Skyriuje *dukterinis juridinis asmuo*, eiktie į **Pagrindinė buhalterijos knyga \> Nustatymai** \> **Sąskaitų grafikas \> Sąskaitų grafikas**.</span><span class="sxs-lookup"><span data-stu-id="1a388-111">In the *subsidiary legal entity*, go to **General ledger \> Setup** \> **Chart of accounts \> Chart of accounts**.</span></span>
2. <span data-ttu-id="1a388-112">Rinkitės sąskaitų grafiką.</span><span class="sxs-lookup"><span data-stu-id="1a388-112">Select a chart of accounts.</span></span> <span data-ttu-id="1a388-113">„FastTab“ **Pagrindinės sąskaitos** rinkitės pagrindinę sąskaitą ir tada **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1a388-113">On the **Main accounts** FastTab, select a main account, and then select **Edit**.</span></span>
3. <span data-ttu-id="1a388-114">Rinkitės kiekvieną dukterinę pagrindinę sąskaitą, kuri turi būti talpinama į konsoliduotą pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1a388-114">Select each subsidiary main account that must be mapped to a consolidated main account.</span></span> <span data-ttu-id="1a388-115">„FastTab“ **Bendri** laukleyje **Konsolidavimo sąskaita** įveskite sąskaitą konsoliduotame juridiniame asmenyje, kurio balansas ar transakcijos turi būti perkeltas į pasirinktos dukterinės pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1a388-115">On the **General** FastTab, in the **Consolidation account** field, enter the account in the consolidated legal entity that the balance or transactions of the selected subsidiary main account must be transferred to.</span></span> <span data-ttu-id="1a388-116">Galite įvesti tą pačią konsoliduotą pagrindinę sąskaitą kelioms dukterinėms sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="1a388-116">You can enter the same consolidated main account for several subsidiary accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a388-117">Jei pagrindiniai dukterinių sąskaitų tipai yra talpiname žemėlapyje ir skiriasi nuo pagrindinių sąskaitos tipų konsoliduotame juridiniame asmenyje, sąskaitų vertės turinčios pagrindinį sąskaitos tipą **Bendri** yra užrašomos konsolidavimo metu.</span><span class="sxs-lookup"><span data-stu-id="1a388-117">If the main account types of the subsidiary accounts that are mapped differ from the main account types of the accounts in the consolidated legal entity, the values of accounts that have a main account type of **Total** are overwritten during consolidation.</span></span>

4. <span data-ttu-id="1a388-118">Parenkite ataskaitas ir finansines ataskaitas konsoliduotam juridiniam asmeniui, kuris yra parengtas pagal finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="1a388-118">Prepare reports and financial statements for the consolidated legal entity that are based on financial dimensions.</span></span> <span data-ttu-id="1a388-119">Atlikite šiuos žingsnius tam, kad talpintumėte finansines dimensijas, kurios naudojamos dukterinėse sąskaitose finansinėse dimensijose konsoliduotame juridiniame asmenyje:</span><span class="sxs-lookup"><span data-stu-id="1a388-119">Follow these steps to map the financial dimensions that are used in the subsidiary accounts to the financial dimensions in the consolidated legal entity:</span></span>

    1. <span data-ttu-id="1a388-120">Skyriuje *Dukterinis juridinis asmuo*, eiktie į **Bendra buhalterijos knyga \> Nustatymai \> Finansinės dimensijos \> Finansinės dimensijos**, rinkitės finansinę dimensiją ir tada rinkitės **Finansinės dimensijos vertės**.</span><span class="sxs-lookup"><span data-stu-id="1a388-120">In the *subsidiary legal entity*, go to **General ledger \> Setup \> Financial dimensions \> Financial dimensions**, select a financial dimension, and then select **Financial dimension values**.</span></span>
    2. <span data-ttu-id="1a388-121">Rinkitės finansinės dimensijos vertę, kad talpintumėte į žemėlapį kitą finansinės dimensijos vertę konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-121">Select the financial dimension value to map to a different financial dimension value in the consolidated legal entity.</span></span>
    3. <span data-ttu-id="1a388-122">„FastTab“ **Bendri** laukelyje **Grupės dimensija** įveskite finansinę dimensiją konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-122">On the **General** FastTab, in the **Group dimension** field, enter the financial dimension in the consolidated legal entity.</span></span> <span data-ttu-id="1a388-123">Konsolidavimo metu, ši finansinė dimensija bus priskirta perlaidoms ir balansams, kurie naudoja pasirinktą finansinę dimensiją dukteriniame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-123">During consolidation, this financial dimension will be assigned to transactions and balances that use the selected financial dimension in the subsidiary legal entity.</span></span> <span data-ttu-id="1a388-124">Finansinės dimensijos, kurias įvedėte čia turi būti naudojamos konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-124">The financial dimensions that you enter here must be used in the consolidated legal entity.</span></span> <span data-ttu-id="1a388-125">Galite priskirti finansinę dimensiją, kuri naudojama kaip grupės finansinė dimensija kelioms dukterinėms finansinėms dimensijoms.</span><span class="sxs-lookup"><span data-stu-id="1a388-125">You can assign the financial dimension that is used as the group financial dimension to several subsidiary financial dimensions.</span></span>

5. <span data-ttu-id="1a388-126">Jei darote interneto konsolidavimą, atlikite šiuos veiksmus siekiant užtikrinti, kad perlaidos atsitinka kaip norite:</span><span class="sxs-lookup"><span data-stu-id="1a388-126">If you're doing an online consolidation, follow these steps to ensure that the transfers occur as you intend:</span></span>

    1. <span data-ttu-id="1a388-127">Skyriuje *konsoliduotas juridinis asmuo*, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[Eksportuoti į\]** norėdami atverti **Konsoliduoti \[Internete\]** puslapį.</span><span class="sxs-lookup"><span data-stu-id="1a388-127">In the *consolidated legal entity*, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Export to\]** to open the **Consolidate \[Online\]** page.</span></span>
    2. <span data-ttu-id="1a388-128">Skirtuke **Kriterijai** rinkitės **Naudoti konsolidavimo sąskaitą** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="1a388-128">On the **Criteria** tab, select the **Use consolidation account** check box.</span></span>
    3. <span data-ttu-id="1a388-129">Skirtuke **Finansinės dimensijos**, rinkitės tinkamas finansines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="1a388-129">On the **Financial dimensions** tab, select the appropriate financial dimensions.</span></span>
    4. <span data-ttu-id="1a388-130">Kiekvienai jūsų pasirinktai finansinei dimensijai, įveskite numerį **Segmento užsakymo** laukelyje siekiant nurodyti užsakymą, kuriame dimensijos turėtų pasirodyti.</span><span class="sxs-lookup"><span data-stu-id="1a388-130">For each financial dimension that you select, enter a number in the **Segment order** field to indicate the order that the dimensions should appear in.</span></span>

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a><span data-ttu-id="1a388-131">Išlaikykite sąskaitų grafiką tą patį dukteriniame ir konsoliduotame juridiniame asmenyje</span><span class="sxs-lookup"><span data-stu-id="1a388-131">Maintain the same chart of accounts in the subsidiary and consolidated legal entities</span></span>

<span data-ttu-id="1a388-132">Pagrindinės sąskaitos dukteriniame juridiniame asmenyje gali turėti tuos pačius sąskaitos numerius ir tą pčią struktūrą sąskaitų grafikui, kaip ir pagrindinės sąskaitos konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-132">The main accounts in the subsidiary legal entity might have the same account numbers and the same structure for the chart of accounts as the main accounts in the consolidated legal entity.</span></span> <span data-ttu-id="1a388-133">Šiuo atveju, jums nereikės rankiniu būdu padaryti pagrindinių sąskaitų žemėlapio dukterinėje įmonėje į pagrindines sąskaitas konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-133">In this case, you don't have to manually map the main accounts in the subsidiary to the main accounts in the consolidated legal entity.</span></span>

<span data-ttu-id="1a388-134">Prieš pradėdami konsolidavimą, imkitės tokių veiksmų.</span><span class="sxs-lookup"><span data-stu-id="1a388-134">Before you start the consolidation, follow these steps.</span></span>

1. <span data-ttu-id="1a388-135">Skyriuje *konsoliduotas juridinis asmuo*, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[Eksportuoti į\]** norėdami atverti **Konsoliduoti \[Internete\]** puslapį.</span><span class="sxs-lookup"><span data-stu-id="1a388-135">In the *consolidated legal entity*, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Export to\]** to open the **Consolidate \[Online\]** page.</span></span>
2. <span data-ttu-id="1a388-136">Rinkitės **Naudokite konsolidavimo sąskaitą** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="1a388-136">Select the **Use consolidation account** check box.</span></span> <span data-ttu-id="1a388-137">Konsolidavimo metu, transakcijos ir balansai bus automatiškai perkeliami į tinkamą sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1a388-137">During consolidation, transactions and balances will automatically be transferred to the correct account.</span></span>

> [!NOTE]
> <span data-ttu-id="1a388-138">Jei sąskaitos neatsako, konsolidavimas sustoja ir gausite pranešimą.</span><span class="sxs-lookup"><span data-stu-id="1a388-138">If the accounts don't correspond, the consolidation stops, and you receive a message.</span></span>

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a><span data-ttu-id="1a388-139">Sukurkite sąskaitų grafiką konsoliduotam juridiniam asmeniui pagal esantį sąskaitų grafiką</span><span class="sxs-lookup"><span data-stu-id="1a388-139">Create a chart of accounts for the consolidated legal entity, based on an existing chart of accounts</span></span>

<span data-ttu-id="1a388-140">Galite daryti konsolidavimą bet jei sąskaitų grafikas dar nebuvo sukurtas konsoliduotame juridiniame asmenyje.</span><span class="sxs-lookup"><span data-stu-id="1a388-140">You can do a consolidation even if a chart of accounts hasn't already been created in the consolidated legal entity.</span></span>

- <span data-ttu-id="1a388-141">Jei planuojate sąskaitos struktūrą, kurią norite naudoti konsoliduotame juridiniame asmenyje, galite talpinti žemėlapį į dukterines sąskaitas šioje struktūroje.</span><span class="sxs-lookup"><span data-stu-id="1a388-141">If you've planned the account structure that you want to use in the consolidated legal entity, you can map the subsidiary accounts to this structure.</span></span>
- <span data-ttu-id="1a388-142">Jei netalpinate jokių dukterinių sąskaitų į žemėlapį, sąskaitos konsoliduotame juridiniame asmenyje yra automatiškai sukuriamos kai dukteriniai duomenys yra perkeliami į konsoliduotą juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="1a388-142">If you don't map any subsidiary accounts, the accounts in the consolidated legal entity are automatically created when subsidiary data is transferred to the consolidated legal entity.</span></span> <span data-ttu-id="1a388-143">Šios sąskaitos yra parengtos pagal pagrindinę sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="1a388-143">These accounts are based on the main account.</span></span> <span data-ttu-id="1a388-144">Tolesni duomenys yra kaupiami sąskaitos konsoliduotame juridiniame asmenyje, kuris turi tą patįį numerį kaip dukterinės sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="1a388-144">Subsequent data is accumulated in accounts in the consolidated legal entity that have the same account number as the subsidiary accounts.</span></span>

<span data-ttu-id="1a388-145">Nepriklausomai nuo to, ar talpinote žemėlapio sąskaitas, pašalinkite **Naudoti konsolidavimo sąskaitą** žymimą laukelį **Konsoliduoti** puslapyje konsoliduotame juridiniame asmenyje prieš vykdydami tokio tipo konsolidavimą.</span><span class="sxs-lookup"><span data-stu-id="1a388-145">Regardless of whether you've mapped accounts, clear the **Use consolidation account** check box on the **Consolidate** page in the consolidated legal entity before you run this type of consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="1a388-146">Galite naudoti šį metodą siekiant sukurti sąskaitų grafiką konsoliduotame juridiniame asmenyje iš sąskaitų grafiko papildomuose juridiniusoe asmenyse.</span><span class="sxs-lookup"><span data-stu-id="1a388-146">You can use this method to create a chart of accounts in the consolidated legal entity from the chart of accounts in one of the subsidiary legal entities.</span></span> <span data-ttu-id="1a388-147">(Dėl papildomos informacijos, žr. [Konsolidavimo paskyros grupės ir papildomos konsolidavimo sąskaitos](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Tuomet priskirkite atitinkamą konsolidavimo konvertavimo principą kiekvienai konsoliduotai pagrindinei sąskaitai ir vykdykite konsolidavimą visiems dukteriniams juridiniams asmenims.</span><span class="sxs-lookup"><span data-stu-id="1a388-147">(For more information, see [Consolidation account groups and additional consolidation accounts](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Then assign an appropriate consolidation conversion principle to each consolidated main account, and run the consolidation for all the subsidiary legal entities.</span></span>