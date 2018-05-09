---
title: "Audito strategijos pažeidimai ir atvejai"
description: "Šiame straipsnyje paaiškinta, kaip sugeneruoti audito atvejus iš audito strategijos taisyklių pažeidimų. Jame taip pat pateikta informacija apie įvairius būdus, kokiais audito strategijoms naudojamas dokumentų pasirinkimo datų diapazonas."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1558b5db36e194a94a829c0a09cc8aa50fbc545b
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="d2737-104">Audito strategijos pažeidimai ir atvejai</span><span class="sxs-lookup"><span data-stu-id="d2737-104">Audit policy violations and cases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2737-105">Šiame straipsnyje paaiškinta, kaip sugeneruoti audito atvejus iš audito strategijos taisyklių pažeidimų.</span><span class="sxs-lookup"><span data-stu-id="d2737-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="d2737-106">Jame taip pat pateikta informacija apie įvairius būdus, kokiais audito strategijoms naudojamas dokumentų pasirinkimo datų diapazonas.</span><span class="sxs-lookup"><span data-stu-id="d2737-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="d2737-107">Kaip generuojami audito atvejai</span><span class="sxs-lookup"><span data-stu-id="d2737-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="d2737-108">Audito strategijos naudojamos nustatant, kurios išlaidų ataskaitos, pirkimo užsakymai ir tiekėjo SF neatitinka verslo taisyklių, kurios nustatomos ir konfigūruojamos kaip audito strategijos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="d2737-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="d2737-109">Audito strategijos vykdomos paketiniu režimu.</span><span class="sxs-lookup"><span data-stu-id="d2737-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="d2737-110">Vykdant audito strategiją, visos strategijos taisyklės, kurios yra tos strategijos dalis, yra vykdomos tuo pačiu metu.</span><span class="sxs-lookup"><span data-stu-id="d2737-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="d2737-111">Kiekviena strategijos taisyklė įvertina dokumentų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="d2737-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="d2737-112">Strategijos taisyklė pasirenka dokumentus, kurie patenka į dokumentų pasirinkimo datų diapazoną ir kurie atitinka nurodytus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="d2737-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="d2737-113">Pavyzdžiui, viena strategijos taisyklė gali pasirinkti išlaidų ataskaitas, kuriose yra valgiai, kainuojantys daugiau nei 50,00.</span><span class="sxs-lookup"><span data-stu-id="d2737-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="d2737-114">Kita strategijos taisyklė gali pasirinkti tiekėjo SF, kurios mokamos konkrečiam tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="d2737-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="d2737-115">Sugeneruojami kiekvieno rinkinyje pasirinkto dokumento pažeidimai.</span><span class="sxs-lookup"><span data-stu-id="d2737-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="d2737-116">Toks pažeidimas yra įrašas, kad konkretus dokumentas, pvz., SF 12345, neatitinka strategijos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="d2737-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="d2737-117">Keli audito pažeidimų įrašai sugrupuojami ir susiejami su audito atvejais.</span><span class="sxs-lookup"><span data-stu-id="d2737-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="d2737-118">Pagal numatytuosius nustatymus kiekvienos audito strategijos atvejus grupuoja audito strategijos taisyklė.</span><span class="sxs-lookup"><span data-stu-id="d2737-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="d2737-119">Jei norite, galite pasirinkti kitus grupavimo kriterijus naudodami puslapį **Atvejų grupavimo kriterijai**.</span><span class="sxs-lookup"><span data-stu-id="d2737-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="d2737-120">Pavyzdžiui, galite grupuoti išlaidų antraštes pagal projekto ID, o tiekėjo SF pagal tiekėjo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="d2737-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="d2737-121">Tokiu atveju, visi išlaidų antraščių pažeidimai, kurie turi tą patį projekto ID, bus sugrupuoti pagal tą patį atvejį, o visos tiekėjų SF, kurios turi tą pačią tiekėjo sąskaitą, taip pat bus sugrupuotos pagal tą patį atvejį.</span><span class="sxs-lookup"><span data-stu-id="d2737-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="d2737-122">Audito strategijos taisyklių, kurios paremtos užklausos tipu **Dublikatas**, pažeidimai nėra grupuojami pagal strategijos taisyklę arba pagal kriterijus, nurodytus puslapyje **Atvejų grupavimo kriterijai**.</span><span class="sxs-lookup"><span data-stu-id="d2737-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="d2737-123">Vietoj to, jie bus grupuojami pagal kriterijus, kurie yra integruoti į audito strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="d2737-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="d2737-124">Pavyzdžiui, jei strategijos taisyklė įvertina išlaidų ataskaitas dėl besidubliuojančių tos pačios sumos išlaidų, prekybininko ID ir datos, visos išlaidos, kurios šiuose laukose turės vienodas reikšmes, bus vienas atvejis.</span><span class="sxs-lookup"><span data-stu-id="d2737-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="d2737-125">Išlaidos, kurios turi skirtingas reikšmes, bus atskiri atvejai.</span><span class="sxs-lookup"><span data-stu-id="d2737-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="d2737-126">Sugeneravus audito atvejus, jie tvarkomi įprastais atvejų valdymo procesais.</span><span class="sxs-lookup"><span data-stu-id="d2737-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="d2737-127">Dokumentų pasirinkimo datų diapazonai</span><span class="sxs-lookup"><span data-stu-id="d2737-127">Document selection date ranges</span></span>
<span data-ttu-id="d2737-128">Vykdant audito strategiją, kiekviena strategijos taisyklė pasirenka nurodyto tipo dokumentus, kurių data patenka į dokumento pasirinkimo datų diapazoną.</span><span class="sxs-lookup"><span data-stu-id="d2737-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="d2737-129">Dokumento pasirinkimo datų diapazonas nurodytas puslapyje **Papildomos parinktys**.</span><span class="sxs-lookup"><span data-stu-id="d2737-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="d2737-130">Daug dokumentų turi daugiau nei vieną su jais siejamą datą.</span><span class="sxs-lookup"><span data-stu-id="d2737-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="d2737-131">Datos laukas, kurį naudoja audito strategijos taisyklė, nurodytas puslapyje **Strategijos taisyklės tipas**.</span><span class="sxs-lookup"><span data-stu-id="d2737-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="d2737-132">Štai keli būdai, kaip audito strategija naudoja dokumentų pasirinkimo datų diapazoną:</span><span class="sxs-lookup"><span data-stu-id="d2737-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="d2737-133">Strategija naudoja kiekvienos strategijos taisyklės versiją, kuri galioja paskutinę dokumentų pasirinkimo datų diapazono dieną.</span><span class="sxs-lookup"><span data-stu-id="d2737-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="d2737-134">Galite peržiūrėti kiekvienos strategijos taisyklės galiojimo datas sąrašo puslapyje **Audito strategijos**.</span><span class="sxs-lookup"><span data-stu-id="d2737-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d2737-135">Strategija naudoja organizacijos mazgus, kurie susiejami su strategija paskutinę dokumentų pasirinkimo datų diapazono dieną.</span><span class="sxs-lookup"><span data-stu-id="d2737-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="d2737-136">Sąrašo puslapyje **Audito strategijos** rodomi tik tie organizacijos mazgai, kurie šiuo metu susieti su strategija.</span><span class="sxs-lookup"><span data-stu-id="d2737-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="d2737-137">Strategijos taisyklių, kurios paremtos užklausos tipu **Sąrašo paieška**, atveju strategija vertina dokumentuose esančius stebimus objektus, kurie tokiais būna paskutinę dokumentų pasirinkimo datų diapazono dieną.</span><span class="sxs-lookup"><span data-stu-id="d2737-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="d2737-138">Daugiau informacijos žr. dalyje [Audito strategijos taisyklės](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="d2737-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>




