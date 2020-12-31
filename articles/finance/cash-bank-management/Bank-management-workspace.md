---
title: Banko valdymo darbo sritis
description: Šioje temoje pateikiama informacijos apie banko valdymo darbo sritį. Šioje darbo srityje nurodoma su įmonės banko sąskaitomis susijusi informacija ir pateikiamas suvestinės rodinys ir analizės puslapis. Suvestinės rodinyje rodomos suvestinės išklotinės, banko sąskaitos informacija, likučio diagrama ir susijusi informacija. Analizės puslapyje naudojantis „Microsoft Power BI“ galimybėmis parodomi su banko sąskaitos likučiais susiję vaizdiniai elementai.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4b7d2da346880278f684a796f2d649e7da52b647
ms.sourcegitcommit: cd83f2bc0e52e13071ad306e07e4c255fc65cb03
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4446177"
---
# <a name="bank-management-workspace"></a><span data-ttu-id="7e648-106">Banko valdymo darbo sritis</span><span class="sxs-lookup"><span data-stu-id="7e648-106">Bank management workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e648-107">Darbo srityje **Banko valdymas** rodoma su įmonės banko sąskaitomis susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="7e648-107">The **Bank management** workspace shows information that is related to company bank accounts.</span></span> <span data-ttu-id="7e648-108">Ši darbo sritis apima rodinį **Suvestinė** ir puslapį **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="7e648-108">This workspace includes a **Summary** view and an **Analytics** page.</span></span> <span data-ttu-id="7e648-109">Rodinyje **Suvestinė** rodomos suvestinės išklotinės, banko sąskaitos informacija, likučio diagrama ir susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="7e648-109">The **Summary** view shows summary tiles, bank account information, a balance chart, and related information.</span></span> <span data-ttu-id="7e648-110">Puslapyje **Analizė** naudojantis „Microsoft Power BI“ galimybėmis parodomi su banko sąskaitos likučiais susiję vaizdiniai elementai.</span><span class="sxs-lookup"><span data-stu-id="7e648-110">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to bank account balances.</span></span>

## <a name="summary-view"></a><span data-ttu-id="7e648-111">Suvestinės rodinys</span><span class="sxs-lookup"><span data-stu-id="7e648-111">Summary view</span></span>

### <a name="summary"></a><span data-ttu-id="7e648-112">Suvestinė</span><span class="sxs-lookup"><span data-stu-id="7e648-112">Summary</span></span>

<span data-ttu-id="7e648-113">Dalyje **Suvestinė** esančiose išklotinėse pateikiama jūsų banko sąskaitų apžvalga ir suteikiama greita prieiga prie dažniausiai naudojamų puslapių.</span><span class="sxs-lookup"><span data-stu-id="7e648-113">The tiles in the **Summary** section give an overview of your bank accounts and provide quick access to the pages that you most often have to use.</span></span> <span data-ttu-id="7e648-114">Banko derinimo informacija yra susijusi su pažangia banko derinimo funkcija.</span><span class="sxs-lookup"><span data-stu-id="7e648-114">The bank reconciliation information is specific to the Advanced bank reconciliation functionality.</span></span> <span data-ttu-id="7e648-115">Įtraukiama informacija tik apie banko sąskaitas, kurioms puslapyje **Banko sąskaita** nustatyta funkcijos **Pažangus banko derinimas** parinktis **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7e648-115">Information is included only for those bank accounts that have the **Advanced bank reconciliation** option set to **Yes** on the **Bank account** page.</span></span> <span data-ttu-id="7e648-116">Dalyje **Suvestinė** galite importuoti banko sąskaitų elektroninius banko failus visiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="7e648-116">From the **Summary** section, you can import electronic bank files for bank accounts across all legal entities.</span></span>

### <a name="bank-accounts"></a><span data-ttu-id="7e648-117">Banko sąskaitos</span><span class="sxs-lookup"><span data-stu-id="7e648-117">Bank accounts</span></span>

<span data-ttu-id="7e648-118">Kiekvienai juridinio subjekto banko sąskaitai dalyje **Banko sąskaitos** skiriama kortelė.</span><span class="sxs-lookup"><span data-stu-id="7e648-118">Each bank account in the legal entity is represented by a card in the **Bank accounts** section.</span></span> <span data-ttu-id="7e648-119">Rodomas dabartinis likutis ir, naudodami detalizavimo funkciją galite rodyti tik tą suvestinę likučio sumą sudarančias operacijas.</span><span class="sxs-lookup"><span data-stu-id="7e648-119">The current balance is shown, and you can drill down to the transactions that make up that summary balance amount.</span></span> <span data-ttu-id="7e648-120">Naudodami sumą **Tarpinės operacijos** taip pat galite detalizuoti, kad būtų rodomos tik tą suvestinę sumą sudarančios operacijos.</span><span class="sxs-lookup"><span data-stu-id="7e648-120">The **Bridged transactions** amount also lets you drill down to the transactions that make up that summary amount.</span></span> <span data-ttu-id="7e648-121">Tarpinės operacijos yra bet kurios laukiančios operacijos, kurios buvo užregistruotos naudojant tarpinį funkcionalumą, bet dar nebuvo apmokėtos.</span><span class="sxs-lookup"><span data-stu-id="7e648-121">Bridged transactions are any pending transactions that have been posted by using bridging functionality, but that haven't yet been cleared.</span></span> <span data-ttu-id="7e648-122">Suma **Laukiantis likutis** yra dabartinis likutis, atėmus tarpines arba laukiančias operacijas.</span><span class="sxs-lookup"><span data-stu-id="7e648-122">The **Pending balance** amount is the current balance minus the bridged, or pending, transactions.</span></span>

<span data-ttu-id="7e648-123">Kortelėje taip pat nurodoma, kada paskutinį kartą suderinta banko sąskaita.</span><span class="sxs-lookup"><span data-stu-id="7e648-123">The card also shows when the bank account was last reconciled.</span></span> <span data-ttu-id="7e648-124">Ši informacija nurodoma tik tuo atveju, jeigu banko sąskaitai įgalinta pažangaus banko derinimo parinktis.</span><span class="sxs-lookup"><span data-stu-id="7e648-124">This information is shown only if Advanced bank reconciliation is enabled for the bank account.</span></span>

### <a name="balance"></a><span data-ttu-id="7e648-125">Likutis</span><span class="sxs-lookup"><span data-stu-id="7e648-125">Balance</span></span>

<span data-ttu-id="7e648-126">Diagramoje **Likutis** nurodoma buvusio banko sąskaitos likučio informacija, kuri pasirinkta dalyje **Banko sąskaitos**, arba visų juridinio subjekto banko sąskaitų informacijos suvestinė.</span><span class="sxs-lookup"><span data-stu-id="7e648-126">The **Balance** chart shows either historic balance information for the bank account that is selected in the **Bank accounts** section or a summary of historic balance information for all bank accounts in the legal entity.</span></span> <span data-ttu-id="7e648-127">Ši informacija pateikiama įvairiems laikotarpiams: dabartinei savaitei, dabartiniam mėnesiui, dabartiniams metams, paskutiniams penkeriems metams ir visiems laikotarpiams (visa banko sąskaitos informacija).</span><span class="sxs-lookup"><span data-stu-id="7e648-127">This information is available for various periods: the current week, the current month, the current year, the last five years, and all periods (the full history of the bank account).</span></span> 

<span data-ttu-id="7e648-128">Jei peržiūrite vienos banko sąskaitos diagramą **Likutis**, ankstesni likučiai rodomi banko sąskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="7e648-128">If you're viewing the **Balance** chart for a single bank account, the historic balances are shown in the bank account currency.</span></span> <span data-ttu-id="7e648-129">Jei peržiūrite visų juridinio subjekto banko sąskaitų diagramą, ankstesni likučiai rodomi apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="7e648-129">If you're viewing the chart for all bank accounts in the legal entity, the historic balances are shown in the accounting currency.</span></span>

<span data-ttu-id="7e648-130">Informacija apie tai, kada paskutinį kartą atnaujinti duomenys, rodoma diagramos viršuje.</span><span class="sxs-lookup"><span data-stu-id="7e648-130">Information about when the data was last updated appears at the top of the chart.</span></span> <span data-ttu-id="7e648-131">Galite atnaujinti duomenis pagal tai, ko jums reikia.</span><span class="sxs-lookup"><span data-stu-id="7e648-131">You can update the data as you require.</span></span>

### <a name="related-information"></a><span data-ttu-id="7e648-132">Susijusi informacija</span><span class="sxs-lookup"><span data-stu-id="7e648-132">Related information</span></span>

<span data-ttu-id="7e648-133">Dalyje **Susijusi informacija** atidarę puslapį **Pagrindinis žurnalas** galite atlikti banko pavedimus.</span><span class="sxs-lookup"><span data-stu-id="7e648-133">From the **Related information** section, you can open the **General journal** page to complete bank transfers.</span></span> <span data-ttu-id="7e648-134">Taip pat galite greitai atidaryti puslapius **Banko operacijos** ir **Tarpinės operacijos**.</span><span class="sxs-lookup"><span data-stu-id="7e648-134">You can also quickly open the **Bank transactions** and **Bridged transactions** pages.</span></span>

## <a name="analytics-view"></a><span data-ttu-id="7e648-135">Analizės rodinys</span><span class="sxs-lookup"><span data-stu-id="7e648-135">Analytics view</span></span>

<span data-ttu-id="7e648-136">Puslapyje **Analizė** pateikiamos svarbios dabartinės įmonės banko sąskaitų metrikos.</span><span class="sxs-lookup"><span data-stu-id="7e648-136">The **Analytics** page provides important metrics about the bank accounts in the current company.</span></span> <span data-ttu-id="7e648-137">Šiame puslapyje pateikiami toliau nurodomi vaizdo elementai.</span><span class="sxs-lookup"><span data-stu-id="7e648-137">The following visualizations are available on the page:</span></span>

-   <span data-ttu-id="7e648-138">Banko likutis sistemos valiuta</span><span class="sxs-lookup"><span data-stu-id="7e648-138">Total bank balance in system currency</span></span>
-   <span data-ttu-id="7e648-139">Likutis pagal juridinį subjektą</span><span class="sxs-lookup"><span data-stu-id="7e648-139">Balance by legal entity</span></span>
-   <span data-ttu-id="7e648-140">Šiandienos faktinis ir prognozuojamas likutis banko sąskaitos valiuta</span><span class="sxs-lookup"><span data-stu-id="7e648-140">Today’s actual vs forecasted balance in bank account currency</span></span>
-   <span data-ttu-id="7e648-141">Likutis pagal banko sąskaitą</span><span class="sxs-lookup"><span data-stu-id="7e648-141">Balance by bank account</span></span>
-   <span data-ttu-id="7e648-142">Balansas pagal valiutą</span><span class="sxs-lookup"><span data-stu-id="7e648-142">Balance by currency</span></span>

<span data-ttu-id="7e648-143">Darbo srityje **Grynųjų pinigų peržiūra – visos įmonės** galite peržiūrėti visų įmonių banko analizės informaciją.</span><span class="sxs-lookup"><span data-stu-id="7e648-143">You can view bank analytics across all companies from the **Cash overview – all companies** workspace.</span></span> <span data-ttu-id="7e648-144">Daugiau informacijos žr. [„Power BI“ turinys Grynųjų pinigų apžvalga](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="7e648-144">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>
