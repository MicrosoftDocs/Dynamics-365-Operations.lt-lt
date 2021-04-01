---
title: Parengti juridinį asmenį konsolidavimo procesui
description: Konsolidavimo metu renkate transakcija iš kelių juridinių asmenų rinkinių sąskaitų į vieną juridinių asmenų sąskaitų rinkinį. Šioje temoje paaiškinama, kaip parengti juridinį asmenį konsolidavimui.
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
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 07988e71276c6439e392bce2087f3a8923f5f40b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230207"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="29abe-104">Parengti juridinį asmenį konsolidavimo procesui</span><span class="sxs-lookup"><span data-stu-id="29abe-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29abe-105">Konsolidavimo metu renkate transakcija iš kelių juridinių asmenų rinkinių sąskaitų į vieną juridinių asmenų sąskaitų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="29abe-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="29abe-106">Šioje temoje paaiškinama, kaip parengti juridinį asmenį konsolidavimui.</span><span class="sxs-lookup"><span data-stu-id="29abe-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="29abe-107">Rekomenduojame jums naudoti „Management Reporter“ „Microsoft Dynamics 365 Finance“ siekiant suderinti finansinius rezultatus keliems juridiniams asmenims konsoliduotame formate.</span><span class="sxs-lookup"><span data-stu-id="29abe-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="29abe-108">„Management Reporter“ leidžia jums kurti konsoliduotas finansines ataskaitas juridiniuose objektuose, naudoti „Exce“ siekiant importuoti konsolidavimo duomenis iš kitų šaltinių ir versti sumas į bet kokių ataskaitų valiutų skaičius be poreikio vykdyti konsolidavimo procesą „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="29abe-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="29abe-109">Galite spausdinti ataskaitas, tokias kaip finansinės ataskaitos iš konsoliduoto juridinio asmens.</span><span class="sxs-lookup"><span data-stu-id="29abe-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="29abe-110">Nepaisant to, negalite naudoti konsoliduoto juridinio asmens kasdienėms transakcijoms.</span><span class="sxs-lookup"><span data-stu-id="29abe-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="29abe-111">Galite konsoliduoti duomenis iš juridinių asmenų, kurie naudoja kitas duomenų bazes nei konsoliduotas juridinis asmuo.</span><span class="sxs-lookup"><span data-stu-id="29abe-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="29abe-112">Toks konsolidavimo procesas yra vadinamas *importuoti konsolidavimą*.</span><span class="sxs-lookup"><span data-stu-id="29abe-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="29abe-113">Kitu atveju, juridiniai asmenys gali naudot tą pačią duomenų bazę kaip konsoliduotas juridinis asmuo.</span><span class="sxs-lookup"><span data-stu-id="29abe-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="29abe-114">Toks konsolidavimo procesas yra vadinamas *internetiniu konsolidavimu*.</span><span class="sxs-lookup"><span data-stu-id="29abe-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="29abe-115">Konsoliduotas juridinis asmuo renka dukterinių bendrovių rezultatus ir balansus.</span><span class="sxs-lookup"><span data-stu-id="29abe-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="29abe-116">Norėdami parengti konsoliduotą juridinį asmenį konsolidavimui, vadovaukitės šiais žingsniais.</span><span class="sxs-lookup"><span data-stu-id="29abe-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="29abe-117">Eikite į **Bendra buhalterinė knyga \> Nustatymai \> Organizacija \> Jurdiniai asmenys**.</span><span class="sxs-lookup"><span data-stu-id="29abe-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="29abe-118">Rinkitės **Naujas** norėdami sukurti juridinį asmenį, kuris bus konsoliduotas juridinis asmuo.</span><span class="sxs-lookup"><span data-stu-id="29abe-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="29abe-119">Rinkitės **Naudoti finansinio konsolidavimo proceso** žymimą laukelį ir tuomet įveskite informaciją apie konsoliduotą juridinį asmenį.</span><span class="sxs-lookup"><span data-stu-id="29abe-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="29abe-120">Įsitikinkite, kad įvedėte šią informaciją tiksliai kaip norite ją parodyti konsoliduoto juridinio asmens finansinėse ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="29abe-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="29abe-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="29abe-121">Close the page.</span></span>
5. <span data-ttu-id="29abe-122">Rinkitės konsoliduotą juridinį asmenį laukelyje dešiniame viršutiniame puslapio kampe ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="29abe-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="29abe-123">Eikite į **Bendra buhalterinė knyga \> Nustatymai \> Buhalterinė knyga**.</span><span class="sxs-lookup"><span data-stu-id="29abe-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="29abe-124">Rinkitės sąskaitų grafikus, mokesčių kalendorių, apskaitos valiutą, pasirenkamą ataskaitos valiutą ir numatytą keitimo kurso tipą konsoliduotam juridiniam asmeniui.</span><span class="sxs-lookup"><span data-stu-id="29abe-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="29abe-125">Eikite į **Buhalterinė knyga \> Nustatymai \> Valiuta \> Keitimo kurso valiuta**.</span><span class="sxs-lookup"><span data-stu-id="29abe-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="29abe-126">Nustatykite valiutos keitimo kursus atitinkamiems dukterinių juridinių asmenų valiutų laikotarpiams.</span><span class="sxs-lookup"><span data-stu-id="29abe-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="29abe-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="29abe-127">Close the page.</span></span>
11. <span data-ttu-id="29abe-128">Jei konsoliduotas juridinis asmuo turi dukterinių įmonių, naudojančių užsienio valiutas, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="29abe-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="29abe-129">Eikite į **Bendra buhalterinė knyga \> Nustatymai \> Publikavimas \> Sąskaitos automatinėms transakcijoms**.</span><span class="sxs-lookup"><span data-stu-id="29abe-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="29abe-130">Laukelyje **Publikavimo tipas** rinkitės atitinkamą sąskaitą:</span><span class="sxs-lookup"><span data-stu-id="29abe-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="29abe-131">Jei juridinis asmuo turi užsienio dukterines įmones, kurios yra finansiškai ar savo veikla priklausomos nuo valdančio juridinio asmens, rinkitės atitinkamą sąskaitą **Pelno ir nuostolių sąskaitą konsolidavimo skirtumams** publikavimo tipą.</span><span class="sxs-lookup"><span data-stu-id="29abe-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="29abe-132">Jei konsoliduojate dukterinę įmonę, kuri yra finansiškai ir savo veikla nepriklausoma nuo valdančio juridinio asmens ar juridinio asmens, turinčio kelių dukterinių įmonių rezultatus, finansiškai ir savo veikla nepriklausančių nuo valdančio juridinio asmens ir jei naudojate vertimo metodus siekiant konsoliduoti duomenis, rinkitės atitinkamą sąskaitą **Balanso sąskaita konsolidavimo skirtumams** publikavimo tipą.</span><span class="sxs-lookup"><span data-stu-id="29abe-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="29abe-133">Laukelyje **Pagrindinė sąskaitą**, rinkitės pagrindines sąskaitas, kurios turi būti naudojamos užsienio valiutos pakartotinio įvertinimo keitimams.</span><span class="sxs-lookup"><span data-stu-id="29abe-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="29abe-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="29abe-134">Close the page.</span></span>

    <span data-ttu-id="29abe-135">Jei sukuriate konsoliduotą juridinį asmenį periodo pradžioje, galite iš naujo įvertinti užsienio valiutos sumas kaip keitimo valiutų kursą konsolidavimo metu.</span><span class="sxs-lookup"><span data-stu-id="29abe-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="29abe-136">Konsoliduotas juridinis asmuo dabar yra nustatytas **Konsolidavimo** periodiniame darbe.</span><span class="sxs-lookup"><span data-stu-id="29abe-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="29abe-137">Galite importuoti konsolidavimą ar atlikti konsolidavimą internete.</span><span class="sxs-lookup"><span data-stu-id="29abe-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="29abe-138">Norėdami atlikti importavimo konsolidavimą, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[importuoti iš\]**.</span><span class="sxs-lookup"><span data-stu-id="29abe-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="29abe-139">Norėdami konsoliduoti internetu, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[internetu\]**.</span><span class="sxs-lookup"><span data-stu-id="29abe-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="29abe-140">Prieš tai, kai galite sutvarkyti konsolidavimą, turite parengti dukterinį juridinį asmenį konsolidavimui.</span><span class="sxs-lookup"><span data-stu-id="29abe-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="29abe-141">Dėl daugiau informacijos, žr. [Nustatykite dukterinį juridinį asmenį konsolidavimui](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="29abe-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]