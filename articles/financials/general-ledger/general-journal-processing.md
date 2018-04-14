---
title: "Bendrųjų žurnalų apdorojimas"
description: "Šiame straipsnyje aprašytos programos „Microsoft Dynamics 365 for Finance and Operations“ galimybės, galinčios padėti lengviau atlikti bendrąjį žurnalo apdorojimą, taip pat gali padėti užtikrinti, kad užfiksuoti tinkami duomenys ir nėra pažeidžiama vidinė kontrolė."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 038833752f5e96055fc1449a473705ecd937b5a4
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="f9c2c-103">Bendrųjų žurnalų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="f9c2c-103">General journal processing</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f9c2c-104">Šiame straipsnyje aprašytos programos „Microsoft Dynamics 365 for Finance and Operations“ galimybės, galinčios padėti lengviau atlikti bendrąjį žurnalo apdorojimą, taip pat gali padėti užtikrinti, kad užfiksuoti tinkami duomenys ir nėra pažeidžiama vidinė kontrolė.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="f9c2c-105">Žurnalų pavadinimai</span><span class="sxs-lookup"><span data-stu-id="f9c2c-105">Journal names</span></span>

<span data-ttu-id="f9c2c-106">Viena iš svarbiausių sričių, kurias reikia nustatyti, yra žurnalų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="f9c2c-107">Naudinga apibrėžti konkrečius žurnalų pavadinimus kiekvienam tikslui, pavyzdžiui, vidinės įmonės, kaupimo koregavimo ir klaidų taisymo.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="f9c2c-108">Galite pritaikyti kiekvieno žurnalo pavadinimą, kad įvesti duomenis kiekvienu tikslu būtų lengva ir saugu.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="f9c2c-109">Puslapyje **Žurnalų pavadinimai** galite nustatyti šiuos elementus.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="f9c2c-110">**Darbo eigos patvirtinimas** – norėdami padidinti vidinę kontrolę, apibrėžkite žurnalo darbo eigas, nustatančias peržiūros ir patvirtinimo veiksmų svarbos ribas pagal tokius kriterijus kaip bendroji debeto suma.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="f9c2c-111">Galite nustatyti bendrųjų žurnalų darbo eigas puslapyje **Didžiosios knygos darbo eigos**.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="f9c2c-112">**Numatytosios reikšmės** – pasirinkite numatytąsias korespondentinių sąskaitų, valiutos ir finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="f9c2c-113">**Žurnalo valdymas** – galite nustatyti įmonės ir sąskaitos tipo apribojimus, taip pat segmentų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="f9c2c-114">**Pavyzdžiai**</span><span class="sxs-lookup"><span data-stu-id="f9c2c-114">**Examples**</span></span>

<span data-ttu-id="f9c2c-115">Žurnalo pavadinimą galima naudoti tik koreguoti.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="f9c2c-116">Tokiu atveju galite nurodyti, kad visoms įmonėms tinkamas tik sąskaitos tipas **Didžioji knyga**.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="f9c2c-117">[![Žurnalų kontrolės sąskaitos tipai](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="f9c2c-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="f9c2c-118">Žurnalo pavadinimą galima naudoti tik konkrečiam segmentui arba pagrindinių sąskaitų diapazonui.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="f9c2c-119">[![Žurnalų kontrolės segmentas](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="f9c2c-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="f9c2c-120">Parinktis **Automatinis atšaukimas** yra bendruosiuose žurnaluose.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="f9c2c-121">Pavyzdžiui, turite kaupimo koregavimą, kurio faktinis dokumentas dar neapdorotas, kaip pavaizduota šioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="f9c2c-122">[![Pagrindinio žurnalo atšaukimas](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="f9c2c-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="f9c2c-123">„Microsoft Excel“ papildinys, skirtas žurnalo įrašams, teikia papildomą automatizavimo lygį ir palengvina duomenų įvedimą.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="f9c2c-124">Veiksmas **Atidaryti eilutes programoje „Excel“** galimas puslapiuose **Pagrindinis žurnalas** ir **Žurnalo kvitas**.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="f9c2c-125">Puslapyje **Periodiniai žurnalai** galite nustatyti pasikartojančius žurnalus, kad žurnalų apdorojimas būtų automatizuotas.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="f9c2c-126">Bet kada galite naudoti kvitų šablonus.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="f9c2c-127">Puslapio **Pagrindiniai žurnalai** puslapyje **Žurnalo kvitas**, dalyje **Funkcijos**, rasite veiksmus **Įrašyti** ir **Pasirinkti kvito šabloną**.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="f9c2c-128">Susijusi sąranka</span><span class="sxs-lookup"><span data-stu-id="f9c2c-128">Related setup</span></span>
<span data-ttu-id="f9c2c-129">Ši sąranka nėra susijusi su pagrindiniais žurnalais, bet padės užtikrinti, kad bus įrašomi teisingi duomenys ir įrašyti bus lengva.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="f9c2c-130">Korespondentinė sąskaita, subsąskaita</span><span class="sxs-lookup"><span data-stu-id="f9c2c-130">Main account</span></span>

<span data-ttu-id="f9c2c-131">Pagrindinės sąskaitos sąranka teikia daug pagrindinio žurnalo apdorojimo galimybių.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="f9c2c-132">**DC / RC reikalavimas** – naudokite šią parinktį, jei pagrindinė sąskaita naudojama tik debeto arba kredito operacijoms.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="f9c2c-133">Sąranka patikrinama, kai žurnalą tikrinamas arba registruojamas.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="f9c2c-134">**Numatytoji korespondentinė sąskaita**</span><span class="sxs-lookup"><span data-stu-id="f9c2c-134">**Default offset account**</span></span>
-   <span data-ttu-id="f9c2c-135">**Sustabdyta** – sustabdykite visų įmonių arba konkrečios įmonės / juridinių subjektų duomenų įvedimą pagrindinėje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="f9c2c-136">**Neleisti įvesti rankiniu būdu** – neleidžia vartotojams įvesti sąskaitos reikės žurnaluose rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="f9c2c-137">**Numatytoji reikšmė / tikrinti valiutą**</span><span class="sxs-lookup"><span data-stu-id="f9c2c-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="f9c2c-138">**Juridinio subjekto nepaisymas** – ši sąranka taikoma apibrėžtai įmonei / juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="f9c2c-139">**Numatytoji reikšmė / tikrinti PVM**</span><span class="sxs-lookup"><span data-stu-id="f9c2c-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="f9c2c-140">**Numatytoji dimensija** – **Nefiksuota** arba **Fiksuota reikšmė**.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="f9c2c-141">**Fiksuota reikšmė** padės užtikrinti, kad visada registruojant iš šios pagrindinės sąskaitos bus naudojama dimensijos reikšmė, nustatyta **Fiksuota**.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="f9c2c-142">**Registravimo tikrinimas**</span><span class="sxs-lookup"><span data-stu-id="f9c2c-142">**Posting validation**</span></span>
    -   <span data-ttu-id="f9c2c-143">**Vartotojo tikrinimas** – šia parinktimi valdoma, kurie vartotojai gali registruoti pagrindinėje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="f9c2c-144">**Registravimo tipo tikrinimas** – šia parinktimi valdoma, kurie registravimo pagrindinėje sąskaitoje tipai yra leidžiami.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="f9c2c-145">Apskaitos struktūros ir išplėstinių taisyklių struktūros</span><span class="sxs-lookup"><span data-stu-id="f9c2c-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="f9c2c-146">Apskaitos struktūros ir išplėstinių taisyklių struktūros yra labai svarbios siekiant užtikrinti, kad duomenys, būtini finansinėms ataskaitoms ir efektyvumui sekti, būtų įrašomi apdorojant bendrąjį žurnalą ir dokumentuojant.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="f9c2c-147">Apskaitos struktūros ir išplėstinių taisyklių struktūros leidžia pritaikyti duomenų įvedimo patirtį.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="f9c2c-148">Galite leisti tik kiekvienu atveju svarbių finansinių dimensijų duomenų įrašus, taip pat galite taikyti reikalavimą, kad privalomi ir teisingi duomenys visada būtį įrašomi.</span><span class="sxs-lookup"><span data-stu-id="f9c2c-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="f9c2c-149">Daugiau informacijos ieškokite šiose temose:</span><span class="sxs-lookup"><span data-stu-id="f9c2c-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="f9c2c-150">[Planavimas: sąskaitų planas](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="f9c2c-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="f9c2c-151">Kurti papildomas žurnalų taisykles</span><span class="sxs-lookup"><span data-stu-id="f9c2c-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="f9c2c-152">Kurti žurnalo įrašą naudojant šabloną</span><span class="sxs-lookup"><span data-stu-id="f9c2c-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="f9c2c-153">Kurti ir patvirtinti žurnalus</span><span class="sxs-lookup"><span data-stu-id="f9c2c-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="f9c2c-154">Registruoti periodinius žurnalus</span><span class="sxs-lookup"><span data-stu-id="f9c2c-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="f9c2c-155">Apdoroti didžiosios knygos paskirstymo žurnalą</span><span class="sxs-lookup"><span data-stu-id="f9c2c-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



