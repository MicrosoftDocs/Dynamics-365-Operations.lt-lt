---
title: "SF patvirtinimai mobiliąja programa"
description: "Šioje temoje pateikiamas praktinis mobiliųjų įrenginių scenarijų kūrimo metodas programoje „Dynamics 365 for Finance and Operations‟, pavyzdyje naudojant tiekėjo SF tvirtinimus mobiliuosiuose įrenginiuose."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0e1b3382bc244996231bfb20f6d65ef2d07aef3a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="mobile-invoice-approvals"></a><span data-ttu-id="6a032-103">SF patvirtinimai mobiliąja programa</span><span class="sxs-lookup"><span data-stu-id="6a032-103">Mobile invoice approvals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6a032-104">„Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ mobiliųjų įrenginių galimybės verslo vartotojui suteikia galimybę kurti mobiliąją patirtį.</span><span class="sxs-lookup"><span data-stu-id="6a032-104">Mobile capabilities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition let a business user design mobile experiences.</span></span> <span data-ttu-id="6a032-105">Sudėtingesniais scenarijais platforma taip pat suteikia galimybę kūrėjams pagal poreikį galimybes išplėsti.</span><span class="sxs-lookup"><span data-stu-id="6a032-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="6a032-106">Efektyviausias būdas susipažinti su kai kuriomis naujomis mobiliųjų įrenginių sąvokomis yra peržiūrėti kelių scenarijų kūrimo procesą.</span><span class="sxs-lookup"><span data-stu-id="6a032-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="6a032-107">Šioje temoje pateikiamas praktinis mobiliųjų įrenginių scenarijų kūrimo metodas, pavyzdyje naudojant tiekėjo SF tvirtinimus mobiliuosiuose įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="6a032-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="6a032-108">Ši tema turėtų padėti sukurti kitus scenarijų variantus ir pritaikyti žinias kitiems scenarijams, kurie nėra susiję su tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="6a032-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="6a032-109">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="6a032-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="6a032-110">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="6a032-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="6a032-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="6a032-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a032-112">Išankstinis mobiliųjų įrenginių vadovo perskaitymas</span><span class="sxs-lookup"><span data-stu-id="6a032-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="6a032-113">Mobilioji platforma</span><span class="sxs-lookup"><span data-stu-id="6a032-113">Mobile platform</span></span>](/dynamics365/unified-operations/dev-itpro/mobile-apps/platform/mobile-platform-home-page)                                                                                                  |
| <span data-ttu-id="6a032-114">„Dynamics 365 for Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="6a032-114">Dynamics 365 for Finance and Operations</span></span>                                                                             | <span data-ttu-id="6a032-115">Aplinka, kurioje yra „Microsoft Dynamics 365 for Operations“ 1611 versijos ir „Microsoft Dynamics for Operations“ 3 platformos naujinimas (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="6a032-115">An environment that has Microsoft Dynamics 365 for Operations version 1611 and Microsoft Dynamics for Operations platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="6a032-116">Įdiekite karštąsias pataisas KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="6a032-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="6a032-117">Užduočių įrašymo priemonė gali klaidingai įrašyti dvi išplečiamųjų dialogų komandas Uždaryti; tai įtraukta į „Dynamics 365 for Operations“ 3 platformos naujinį (2016 m. lapkričio mėn. naujinys)</span><span class="sxs-lookup"><span data-stu-id="6a032-117">Task recorder can erroneously record two Close commands for dropdown dialogs this is included in Dynamics 365 for Operation platform update 3 (November 2016 update)</span></span> |
| <span data-ttu-id="6a032-118">Įdiekite karštąsias pataisas KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="6a032-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="6a032-119">Įdiegus šias karštąsias pataisas priedus galima peržiūrėti mobiliajame kliente; tai įtraukta į „Dynamics 365 for Operations“ 3 platformos naujinį (2016 m. lapkričio mėn. naujinys).</span><span class="sxs-lookup"><span data-stu-id="6a032-119">This hotfix enables attachments to be viewed on the mobile client this is included in Dynamics 365 for Operation platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="6a032-120">Įdiekite karštąsias pataisas KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="6a032-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="6a032-121">Tiekėjo SF mobiliuosiuose įrenginiuose tvirtinimo programos kodas; tai įtraukta į „Microsoft Dynamics AX“ 7.0.1 programos versiją (2016 m. gegužės mėn.).</span><span class="sxs-lookup"><span data-stu-id="6a032-121">Application code for the mobile vendor invoice approval application this is included in Microsoft Dynamics AX application 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="6a032-122">„Android“, „iOS“ arba „Windows“ įrenginys, kuriame įdiegta „Finance and Operations“ mobilioji programa</span><span class="sxs-lookup"><span data-stu-id="6a032-122">An Android or iOS or a Windows device that has the mobile app installed for Finance and Operations</span></span> | <span data-ttu-id="6a032-123">Ieškokite programos atitinkamoje programų parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="6a032-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="6a032-124">Įžanga</span><span class="sxs-lookup"><span data-stu-id="6a032-124">Introduction</span></span>
<span data-ttu-id="6a032-125">Norint tiekėjo SF tvirtinti mobiliuosiuose įrenginiuose, reikia įdiegti tris karštąsias pataisas, paminėtas skyriuje „Būtinosios sąlygos“.</span><span class="sxs-lookup"><span data-stu-id="6a032-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="6a032-126">Šios karštosios pataisos nepateikia SF tvirtinimo darbo srities.</span><span class="sxs-lookup"><span data-stu-id="6a032-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="6a032-127">Norėdami sužinoti, kas yra darbo sritis mobiliųjų įrenginių kontekste, perskaitykite mobiliųjų įrenginių vadovą, paminėtą skyriuje „Būtinosios sąlygos“.</span><span class="sxs-lookup"><span data-stu-id="6a032-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="6a032-128">SF tvirtinimo darbo sritį reikia sukurti.</span><span class="sxs-lookup"><span data-stu-id="6a032-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="6a032-129">Kiekviena organizacija skirtingai planuoja ir nustato tiekėjo SF verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="6a032-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="6a032-130">Prieš kurdami tiekėjo SF tvirtinimo mobiliuosiuose įrenginiuose patirtį, atsižvelkite į toliau nurodytus verslo proceso aspektus.</span><span class="sxs-lookup"><span data-stu-id="6a032-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="6a032-131">Tikslas yra kiek įmanoma labiau naudoti šiuos duomenų taškus ir optimizuoti vartotojo patirtį mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="6a032-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="6a032-132">Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="6a032-133">Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="6a032-134">Kiek SF yra SF eilučių?</span><span class="sxs-lookup"><span data-stu-id="6a032-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="6a032-135">Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</span><span class="sxs-lookup"><span data-stu-id="6a032-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="6a032-136">Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</span><span class="sxs-lookup"><span data-stu-id="6a032-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="6a032-137">Jei atsakymas į šį klausimą yra teigiamas, atsižvelkite į tolesnius klausimus.</span><span class="sxs-lookup"><span data-stu-id="6a032-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="6a032-138">Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos, skaidymai ir t. t.)?</span><span class="sxs-lookup"><span data-stu-id="6a032-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="6a032-139">Vėl taikykite 80 / 20 taisyklę.</span><span class="sxs-lookup"><span data-stu-id="6a032-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="6a032-140">Ar SF antraštėje taip pat yra apskaitos paskirstymų?</span><span class="sxs-lookup"><span data-stu-id="6a032-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="6a032-141">Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-141">If so, should these accounting distributions be available on the device?</span></span>

> [!NOTE]
> <span data-ttu-id="6a032-142">Šioje temoje nepaaiškinama, kaip redaguoti apskaitos paskirstymus, nes mobiliųjų įrenginių scenarijuose ši funkcija šiuo metu nepalaikoma.</span><span class="sxs-lookup"><span data-stu-id="6a032-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="6a032-143">Ar vartotojai įrenginyje norės matyti SF priedus?</span><span class="sxs-lookup"><span data-stu-id="6a032-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="6a032-144">SF tvirtinimo mobiliuosiuose įrenginiuose patirties kūrimas skirsis, priklausomai nuo atsakymų į šiuos klausimus.</span><span class="sxs-lookup"><span data-stu-id="6a032-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="6a032-145">Tikslas yra optimizuoti organizacijos verslo proceso valdymo mobiliuosiuose įrenginiuose vartotojo patirtį.</span><span class="sxs-lookup"><span data-stu-id="6a032-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="6a032-146">Likusioje šios temos dalyje peržiūrėsime du scenarijų variantus, kurie pagrįsti skirtingais atsakymais į ankstesnius klausimus.</span><span class="sxs-lookup"><span data-stu-id="6a032-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="6a032-147">Paprastai dirbant su mobiliųjų įrenginių dizaino įrankiu patariama nepamiršti publikuoti keitimų, kad neprarastumėte naujinimų.</span><span class="sxs-lookup"><span data-stu-id="6a032-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="6a032-148">„Contoso“ paprasto SF tvirtinimo scenarijaus kūrimas</span><span class="sxs-lookup"><span data-stu-id="6a032-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a032-149">Scenarijaus atributas</span><span class="sxs-lookup"><span data-stu-id="6a032-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="6a032-150">Atsakymas</span><span class="sxs-lookup"><span data-stu-id="6a032-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a032-151">Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="6a032-152">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="6a032-152">Vendor name</span></span></li>
<li><span data-ttu-id="6a032-153">Bendroji SF suma</span><span class="sxs-lookup"><span data-stu-id="6a032-153">Invoice total</span></span></li>
<li><span data-ttu-id="6a032-154">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="6a032-154">Invoice account</span></span></li>
<li><span data-ttu-id="6a032-155">SF numeris</span><span class="sxs-lookup"><span data-stu-id="6a032-155">Invoice number</span></span></li>
<li><span data-ttu-id="6a032-156">Data</span><span class="sxs-lookup"><span data-stu-id="6a032-156">Invoice date</span></span></li>
<li><span data-ttu-id="6a032-157">SF aprašas</span><span class="sxs-lookup"><span data-stu-id="6a032-157">Invoice description</span></span></li>
<li><span data-ttu-id="6a032-158">Terminas</span><span class="sxs-lookup"><span data-stu-id="6a032-158">Due date</span></span></li>
<li><span data-ttu-id="6a032-159">SF valiuta</span><span class="sxs-lookup"><span data-stu-id="6a032-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a032-160">Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="6a032-161">Įsigijimo kategorija</span><span class="sxs-lookup"><span data-stu-id="6a032-161">Procurement category</span></span></li>
<li><span data-ttu-id="6a032-162">Kiekis</span><span class="sxs-lookup"><span data-stu-id="6a032-162">Quantity</span></span></li>
<li><span data-ttu-id="6a032-163">Vnt. kaina</span><span class="sxs-lookup"><span data-stu-id="6a032-163">Unit price</span></span></li>
<li><span data-ttu-id="6a032-164">Grynoji eilutės suma</span><span class="sxs-lookup"><span data-stu-id="6a032-164">Line net amount</span></span></li>
<li><span data-ttu-id="6a032-165">1099 suma</span><span class="sxs-lookup"><span data-stu-id="6a032-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a032-166">Kiek SF yra SF eilučių?</span><span class="sxs-lookup"><span data-stu-id="6a032-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="6a032-167">Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</span><span class="sxs-lookup"><span data-stu-id="6a032-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="6a032-168">1</span><span class="sxs-lookup"><span data-stu-id="6a032-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a032-169">Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</span><span class="sxs-lookup"><span data-stu-id="6a032-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="6a032-170">Taip</span><span class="sxs-lookup"><span data-stu-id="6a032-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a032-171">Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos ir t. t.)?</span><span class="sxs-lookup"><span data-stu-id="6a032-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="6a032-172">Vėl taikykite 80 / 20 taisyklę.</span><span class="sxs-lookup"><span data-stu-id="6a032-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="6a032-173">Išplėstinė kaina: 2 PVM: 0 Išlaidos: 0</span><span class="sxs-lookup"><span data-stu-id="6a032-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a032-174">Ar SF antraštėje taip pat yra apskaitos paskirstymų?</span><span class="sxs-lookup"><span data-stu-id="6a032-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="6a032-175">Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="6a032-176">Nenaudojama</span><span class="sxs-lookup"><span data-stu-id="6a032-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a032-177">Ar vartotojai įrenginyje norės matyti SF priedus?</span><span class="sxs-lookup"><span data-stu-id="6a032-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="6a032-178">Taip</span><span class="sxs-lookup"><span data-stu-id="6a032-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="6a032-179">Darbo srities kūrimas</span><span class="sxs-lookup"><span data-stu-id="6a032-179">Create the workspace</span></span>

1.  <span data-ttu-id="6a032-180">Naršyklėje atidarykite „Finance and Operations“ ir prisijunkite.</span><span class="sxs-lookup"><span data-stu-id="6a032-180">In a browser, open Finance and Operations, and sign in.</span></span>
2.  <span data-ttu-id="6a032-181">Prisijungę pridėkite dalį **&mode=mobile** prie URL, kaip parodyta tolesniame pavyzdyje, ir atnaujinkite puslapį: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="6a032-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard**&mode=mobile**</span></span>
3.  <span data-ttu-id="6a032-182">Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**.</span><span class="sxs-lookup"><span data-stu-id="6a032-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="6a032-183">Mobiliųjų programų dizaino įrankis pasirodo taip, kaip pasirodo užduočių įrašymo priemonė.</span><span class="sxs-lookup"><span data-stu-id="6a032-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="6a032-184">Spustelėkite **Įtraukti**, kad sukurtumėte naują darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="6a032-185">Šiuo atveju darbo sritį pavadinkite **Mano tvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="6a032-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="6a032-186">Įvesti aprašymą.</span><span class="sxs-lookup"><span data-stu-id="6a032-186">Enter a description.</span></span>
6.  <span data-ttu-id="6a032-187">Pasirinkti darbo srities spalvą.</span><span class="sxs-lookup"><span data-stu-id="6a032-187">Select a workspace color.</span></span> <span data-ttu-id="6a032-188">Darbo srities spalva bus naudojama bendram šios darbo srities mobiliosios patirties stiliui kurti.</span><span class="sxs-lookup"><span data-stu-id="6a032-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="6a032-189">Pasirinkite darbo srities piktogramą.</span><span class="sxs-lookup"><span data-stu-id="6a032-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="6a032-190">Spustelėkite **Atlikta**</span><span class="sxs-lookup"><span data-stu-id="6a032-190">Click **Done**</span></span>
9.  <span data-ttu-id="6a032-191">Spustelėkite **Publikuoti darbo sritį**, kad išsaugotumėte keitimus</span><span class="sxs-lookup"><span data-stu-id="6a032-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="6a032-192">Man priskirtos tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="6a032-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="6a032-193">Pirmasis mobiliųjų įrenginių puslapis, kurį turėtumėte sukurti, yra SF, kurios priskirtos vartotojui peržiūrėti, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="6a032-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="6a032-194">Norėdami kurti šį mobiliųjų įrenginių puslapį, naudokite „Finance and Operations“ puslapį **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="6a032-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page in Finance and Operations.</span></span> <span data-ttu-id="6a032-195">Prieš baigdami šią procedūrą įsitikinkite, kad bent viena tiekėjo SF yra jums priskirta peržiūrėti ir kad SF eilutėje yra du paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="6a032-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="6a032-196">Ši sąranka atitinka šio scenarijaus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="6a032-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="6a032-197">„Finance Operations“ URL pakeiskite meniu elemento pavadinimą į **VendMobileInvoiceAssignedToMeListPage**, kad atidarytumėte sąrašo puslapio **Man priskirtos laukiančios tiekėjo SF** mobiliąją versiją modulyje **Mokėtinos sumos**.</span><span class="sxs-lookup"><span data-stu-id="6a032-197">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="6a032-198">Atsižvelgiant į SF, kurios jūsų sistemoje jums priskirtos, skaičių, šiame puslapyje bus rodomos tos SF.</span><span class="sxs-lookup"><span data-stu-id="6a032-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="6a032-199">Norėdami rasi konkrečią SF, galite naudoti dešinėje pusėje pateiktą filtrą.</span><span class="sxs-lookup"><span data-stu-id="6a032-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="6a032-200">Tačiau šiame pavyzdyje konkreti SF nėra reikalinga.</span><span class="sxs-lookup"><span data-stu-id="6a032-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="6a032-201">Tereikia, kad jums būtų priskirta kokia nors SF, jog galėtumėte kurti mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="6a032-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="6a032-202">Nauji puslapiai, kuriuos galima naudoti, buvo specialiai sukurti tiekėjo SF mobiliųjų įrenginių scenarijams kurti.</span><span class="sxs-lookup"><span data-stu-id="6a032-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="6a032-203">Todėl turite šiuos puslapius naudoti.</span><span class="sxs-lookup"><span data-stu-id="6a032-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="6a032-204">URL turėtų būti toks, kaip toliau toliau, ir įvedus URL turi būti rodomas puslapis su iliustracija: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Puslapis Man priskirtos laukiančios tiekėjo SF](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="6a032-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile [![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
2.  <span data-ttu-id="6a032-205">Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**</span><span class="sxs-lookup"><span data-stu-id="6a032-205">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="6a032-206">Pasirinkite savo darbo sritį ir spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6a032-206">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="6a032-207">Spustelėkite **Įtraukti puslapį**, kad sukurtumėte pirmą mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="6a032-207">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="6a032-208">Įveskite pavadinimą, pvz., **Mano tiekėjo SF**, ir aprašą, pvz., **Man peržiūrėti priskirtos tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="6a032-208">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="6a032-209">Spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="6a032-209">Click **Done**.</span></span>
7.  <span data-ttu-id="6a032-210">Mobiliųjų įrenginių dizaino įrankio skirtuke **Laukai** spustelėkite **Pasirinkti laukus**.</span><span class="sxs-lookup"><span data-stu-id="6a032-210">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="6a032-211">Šio sąrašo puslapio stulpeliuose turi būti tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="6a032-211">The columns on the list page must resemble the following illustration.</span></span> <span data-ttu-id="6a032-212">[![Stulpeliai puslapyje Man priskirtos laukiančios tiekėjo SF](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="6a032-212">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
8.  <span data-ttu-id="6a032-213">Iš sąrašo puslapio įtraukite reikiamus stulpelius, kurie vartotojams turi būti rodomi mobiliųjų įrenginių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="6a032-213">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="6a032-214">Galutiniam vartotojui laukai bus rodomi ta tvarka, kuria juos įtrauksite.</span><span class="sxs-lookup"><span data-stu-id="6a032-214">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="6a032-215">Laukų tvarką galima pakeisti tik iš naujo pažymint visus laukus.</span><span class="sxs-lookup"><span data-stu-id="6a032-215">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="6a032-216">Pagal šio scenarijaus reikalavimus reikalingi aštuoni toliau nurodyti laukai.</span><span class="sxs-lookup"><span data-stu-id="6a032-216">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="6a032-217">Tačiau kai kuriems vartotojams aštuoni laukai gali pasirodyti per didelis informacijos kiekis mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="6a032-217">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="6a032-218">Todėl mobiliųjų įrenginių sąrašo rodinyje bus rodomi tik patys svarbiausi laukai.</span><span class="sxs-lookup"><span data-stu-id="6a032-218">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="6a032-219">Likę laukai bus rodomi informacijos rodinyje, kurį sukursime vėliau.</span><span class="sxs-lookup"><span data-stu-id="6a032-219">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="6a032-220">Dabar įtrauksime toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="6a032-220">For now, we will add the following fields.</span></span> <span data-ttu-id="6a032-221">Spustelėkite šių stulpelių pliuso ženklą (**+**), kad įtrauktumėte į mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="6a032-221">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="6a032-222">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="6a032-222">Vendor name</span></span>
    - <span data-ttu-id="6a032-223">Bendroji SF suma</span><span class="sxs-lookup"><span data-stu-id="6a032-223">Invoice total</span></span>
    - <span data-ttu-id="6a032-224">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="6a032-224">Invoice account</span></span>
    - <span data-ttu-id="6a032-225">SF numeris</span><span class="sxs-lookup"><span data-stu-id="6a032-225">Invoice number</span></span>
    - <span data-ttu-id="6a032-226">Data</span><span class="sxs-lookup"><span data-stu-id="6a032-226">Invoice date</span></span>

    <span data-ttu-id="6a032-227">Įvedus laukus mobiliųjų įrenginių puslapyje turi būti rodoma tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="6a032-227">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    <span data-ttu-id="6a032-228">[![Puslapio rodinys įtraukus laukus](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="6a032-228">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>
9.  <span data-ttu-id="6a032-229">Taip pat dabar turite įtraukti tolesnius stulpelius, kad vėliau galėtumėte įjungti darbo eigos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6a032-229">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="6a032-230">Rodyti baigti užduotį</span><span class="sxs-lookup"><span data-stu-id="6a032-230">Show complete task</span></span>
    - <span data-ttu-id="6a032-231">Rodyti perduoti užduotį</span><span class="sxs-lookup"><span data-stu-id="6a032-231">Show delegate task</span></span>
    - <span data-ttu-id="6a032-232">Rodyti atšaukti užduotį</span><span class="sxs-lookup"><span data-stu-id="6a032-232">Show recall task</span></span>
    - <span data-ttu-id="6a032-233">Rodyti atmesti užduotį</span><span class="sxs-lookup"><span data-stu-id="6a032-233">Show reject task</span></span>
    - <span data-ttu-id="6a032-234">Rodyti prašyti užpildymo užduoties</span><span class="sxs-lookup"><span data-stu-id="6a032-234">Show request completion task</span></span>
    - <span data-ttu-id="6a032-235">Rodyti iš naujo pateikti užduotį</span><span class="sxs-lookup"><span data-stu-id="6a032-235">Show resubmit task</span></span>

10. <span data-ttu-id="6a032-236">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-236">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="6a032-237">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-237">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="6a032-238">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą.</span><span class="sxs-lookup"><span data-stu-id="6a032-238">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="6a032-239">Mokėtinų sumų parametrų formoje, prie dalies **SF** įjunkite parinktį **Laukiančių tiekėjo SF sąraše rodyti bendrą SF sumą**.</span><span class="sxs-lookup"><span data-stu-id="6a032-239">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="6a032-240">Atminkite, kad tik įjungus šį parametrą SF sumos bus apskaičiuotos ir rodomos laukiančių tiekėjo SF sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="6a032-240">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="6a032-241">Ši nauja galimybė yra būtinų karštųjų pataisų 3208224 dalis.</span><span class="sxs-lookup"><span data-stu-id="6a032-241">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="6a032-242">Tiekėjo SF informacija</span><span class="sxs-lookup"><span data-stu-id="6a032-242">Vendor invoice details</span></span>

<span data-ttu-id="6a032-243">Norėdami kurti sąskaitų faktūrų informacijos mobiliųjų įrenginių puslapį, naudokite „Finance and Operations“ puslapį **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="6a032-243">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="6a032-244">Atminkite, kad, atsižvelgiant į SF, kurios sistemoje jums priskirtos, skaičių, šiame puslapyje rodoma seniausia SF (SF, kuri buvo sukurta pirmoji).</span><span class="sxs-lookup"><span data-stu-id="6a032-244">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="6a032-245">Norėdami rasi konkrečią SF, galite naudoti dešinėje pusėje pateiktą filtrą.</span><span class="sxs-lookup"><span data-stu-id="6a032-245">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="6a032-246">Tačiau šiame pavyzdyje konkreti SF nėra reikalinga.</span><span class="sxs-lookup"><span data-stu-id="6a032-246">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="6a032-247">Tereikia kokių nors SF duomenų, kad galėtumėte kurti mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="6a032-247">We just require some invoice data so that we can design the mobile page.</span></span> <span data-ttu-id="6a032-248">[![Darbo eigos puslapis](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="6a032-248">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1.  <span data-ttu-id="6a032-249">„Finance and Operations“ URL pakeiskite meniu elemento pavadinimą įrašydami **VendMobileInvoiceHeaderDetails**, kad atidarytumėte formą</span><span class="sxs-lookup"><span data-stu-id="6a032-249">In the Finance and Operations URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>
2.  <span data-ttu-id="6a032-250">Atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6a032-250">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="6a032-251">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-251">Click the **Edit** button to start edit mode in the workspace.</span></span>
4.  <span data-ttu-id="6a032-252">Pasirinkite puslapį **Mano tiekėjo SF**, kurį sukūrėte anksčiau, o tada spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6a032-252">Select the **My vendor invoices **page that you created earlier, and then click **Edit**.</span></span>
5.  <span data-ttu-id="6a032-253">Skirtuke **Laukai** spustelėkite stulpelio antraštę **Tinklelis**.</span><span class="sxs-lookup"><span data-stu-id="6a032-253">On the **Fields** tab, click the **Grid** column heading.</span></span>
6.  <span data-ttu-id="6a032-254">Spustelėkite **Ypatybės** &gt; **Įtraukti puslapį**.</span><span class="sxs-lookup"><span data-stu-id="6a032-254">Click **Properties** &gt; **Add page**.</span></span> <span data-ttu-id="6a032-255">**Pastaba.** Kai spustelėjate antraštę **Tinklelis** ir įtraukiate puslapį, ryšys su informacijos puslapiu nustatomas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="6a032-255">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>
7.  <span data-ttu-id="6a032-256">Įveskite puslapio pavadinimą, pvz., **SF informacija SF**, ir aprašą, pvz., **SF antraštės ir eilutės informacijos peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="6a032-256">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>
8.  <span data-ttu-id="6a032-257">Spustelėkite **Pasirinkti laukus**.</span><span class="sxs-lookup"><span data-stu-id="6a032-257">Click **Select fields**.</span></span> <span data-ttu-id="6a032-258">Atminkite, kad galutiniam vartotojui laukai bus rodomi ta tvarka, kuria juos įtrauksite.</span><span class="sxs-lookup"><span data-stu-id="6a032-258">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="6a032-259">Laukų tvarką galima pakeisti tik iš naujo pažymint visus laukus.</span><span class="sxs-lookup"><span data-stu-id="6a032-259">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 
9.  <span data-ttu-id="6a032-260">Iš antraštės įtraukite toliau nurodytus laukus, atsižvelgdami į šio scenarijaus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="6a032-260">Add the following fields from the header, based on the requirements for this scenario:</span></span>
    - <span data-ttu-id="6a032-261">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="6a032-261">Vendor name</span></span>
    - <span data-ttu-id="6a032-262">Bendroji SF suma</span><span class="sxs-lookup"><span data-stu-id="6a032-262">Invoice total</span></span>
    - <span data-ttu-id="6a032-263">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="6a032-263">Invoice account</span></span>
    - <span data-ttu-id="6a032-264">SF numeris</span><span class="sxs-lookup"><span data-stu-id="6a032-264">Invoice number</span></span>
    - <span data-ttu-id="6a032-265">Data</span><span class="sxs-lookup"><span data-stu-id="6a032-265">Invoice date</span></span>
    - <span data-ttu-id="6a032-266">SF aprašas</span><span class="sxs-lookup"><span data-stu-id="6a032-266">Invoice description</span></span>
    - <span data-ttu-id="6a032-267">Terminas</span><span class="sxs-lookup"><span data-stu-id="6a032-267">Due date</span></span>
    - <span data-ttu-id="6a032-268">SF valiuta</span><span class="sxs-lookup"><span data-stu-id="6a032-268">Invoice currency</span></span>

10. <span data-ttu-id="6a032-269">Iš puslapio eilučių tinklelio įtraukite toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="6a032-269">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="6a032-270">Įsigijimo kategorija</span><span class="sxs-lookup"><span data-stu-id="6a032-270">Procurement category</span></span>
    - <span data-ttu-id="6a032-271">Kiekis</span><span class="sxs-lookup"><span data-stu-id="6a032-271">Quantity</span></span>
    - <span data-ttu-id="6a032-272">Vnt. kaina</span><span class="sxs-lookup"><span data-stu-id="6a032-272">Unit price</span></span>
    - <span data-ttu-id="6a032-273">Grynoji eilutės suma</span><span class="sxs-lookup"><span data-stu-id="6a032-273">Line net amount</span></span>
    - <span data-ttu-id="6a032-274">1099 suma</span><span class="sxs-lookup"><span data-stu-id="6a032-274">1099 amount</span></span>

11. <span data-ttu-id="6a032-275">Kai visi ankstesniuose dviejuose veiksmuose nurodyti laukai įtraukti, spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="6a032-275">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="6a032-276">Puslapyje turi būti tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="6a032-276">The page must resemble the following illustration.</span></span>
<span data-ttu-id="6a032-277">[![Puslapio rodinys įtraukus laukus](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="6a032-277">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>
12. <span data-ttu-id="6a032-278">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-278">Click **Done** to exit edit mode.</span></span>
13. <span data-ttu-id="6a032-279">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-279">Click **Back** and then **Done** to exit the workspace</span></span>
14. <span data-ttu-id="6a032-280">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="6a032-280">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="6a032-281">Darbo eigos veiksmai</span><span class="sxs-lookup"><span data-stu-id="6a032-281">Workflow actions</span></span>

<span data-ttu-id="6a032-282">Norėdami įtraukti darbo eigos veiksmų, naudokite „Finance and Operations“ puslapį **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="6a032-282">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page in Finance and Operations.</span></span> <span data-ttu-id="6a032-283">Norėdami atidaryti šį puslapį, URL pakeiskite meniu elemento pavadinimą, kaip tai padarėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="6a032-283">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="6a032-284">Tada atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6a032-284">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="6a032-285">Norėdami į informacijos puslapį įtraukti darbo eigos veiksmų, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6a032-285">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="6a032-286">Jums turi būti priskirta tam tikrą būseną turinčių sąskaitų faktūrų, jog kurdami galėtumėte naudoti darbo eigos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6a032-286">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="6a032-287">Darbo eigos veiksmų įrašymas</span><span class="sxs-lookup"><span data-stu-id="6a032-287">Record workflow actions</span></span>
1.  <span data-ttu-id="6a032-288">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-288">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="6a032-289">Pasirinkite puslapį **SF informacija**, kurį sukūrėte anksčiau, o tada spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6a032-289">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="6a032-290">Skirtuke **Veiksmai** spustelėkite **Įtraukti veiksmą**.</span><span class="sxs-lookup"><span data-stu-id="6a032-290">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="6a032-291">Įveskite veiksmo pavadinimą, pvz., **Tvirtinti**, tada įveskite aprašymą, pvz., **Tvirtinti SF**.</span><span class="sxs-lookup"><span data-stu-id="6a032-291">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="6a032-292">Atkreipkite dėmesį, kad čia įvestas veiksmo pavadinimas tampa mobiliojoje programoje vartotojui rodomo veiksmo pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="6a032-292">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="6a032-293">Spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="6a032-293">Click **Done**.</span></span>
6.  <span data-ttu-id="6a032-294">Spustelėkite **Pasirinkti laukus**.</span><span class="sxs-lookup"><span data-stu-id="6a032-294">Click **Select fields**.</span></span>
7.  <span data-ttu-id="6a032-295">Atidarykite darbo eigos procesą puslapyje **VendMobileInvoiceHeaderDetails** ir užbaikite veiksmą, kurį norėjote įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6a032-295">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="6a032-296">Įsitikinkite, kad šio proceso metu įvedėte darbo eigos komentarus, kad į mobiliąją patirtį taip pat būtų įtrauktas komentarų laukas.</span><span class="sxs-lookup"><span data-stu-id="6a032-296">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="6a032-297">Paleidę darbo eigos veiksmą, spustelėkite **Atlikta**, kad baigtumėte užduoti Pasirinkti laukus.</span><span class="sxs-lookup"><span data-stu-id="6a032-297">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="6a032-298">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-298">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="6a032-299">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-299">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="6a032-300">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="6a032-300">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="6a032-301">Pakartodami ankstesnius veiksmus įrašykite visus reikiamus darbo eigos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6a032-301">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="6a032-302">.js failo kūrimas</span><span class="sxs-lookup"><span data-stu-id="6a032-302">Create a .js file</span></span>
1. <span data-ttu-id="6a032-303">Atidarykite „Notepad“ arba „Microsoft Visual Studio“ ir įklijuokite tolesnį kodą.</span><span class="sxs-lookup"><span data-stu-id="6a032-303">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="6a032-304">Įrašykite failą kaip .js failą.</span><span class="sxs-lookup"><span data-stu-id="6a032-304">Save the file as a .js file.</span></span> <span data-ttu-id="6a032-305">Šis kodas atlieka šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="6a032-305">This code does the following:</span></span>
    - <span data-ttu-id="6a032-306">Jis paslepia papildomus su darbo eiga susijusius stulpelius, kuriuos į mobiliųjų įrenginių sąrašo puslapį mes įtraukėme anksčiau.</span><span class="sxs-lookup"><span data-stu-id="6a032-306">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="6a032-307">Šiuos stulpelius mes įtraukėme, kad programai pateiktume informacijos kontekstą ir ji galėtų atlikti kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="6a032-307">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="6a032-308">Atsižvelgiant į aktyvų darbo eigos veiksmą, jis pritaiko logiką, kad būtų rodomi tik tie veiksmai.</span><span class="sxs-lookup"><span data-stu-id="6a032-308">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

> [!NOTE]
> <span data-ttu-id="6a032-309">Kode nurodyti puslapių ir kitų valdiklių pavadinimai turi sutapti su pavadinimais darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="6a032-309">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }

2.  <span data-ttu-id="6a032-310">Įkelkite kodo failą į darbo sritį pasirinkdami skirtuką **Logika**</span><span class="sxs-lookup"><span data-stu-id="6a032-310">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="6a032-311">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-311">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="6a032-312">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-312">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="6a032-313">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="6a032-313">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="6a032-314">Tiekėjo SF priedai</span><span class="sxs-lookup"><span data-stu-id="6a032-314">Vendor invoice attachments</span></span>

1.  <span data-ttu-id="6a032-315">Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**</span><span class="sxs-lookup"><span data-stu-id="6a032-315">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
2.  <span data-ttu-id="6a032-316">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-316">Click the **Edit** button to start edit mode in the workspace.</span></span>
3.  <span data-ttu-id="6a032-317">Pasirinkite puslapį **SF informacija**, kurį sukūrėte anksčiau, o tada spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6a032-317">Select the **Invoice details **page that you created earlier, and then click **Edit**.</span></span>
4.  <span data-ttu-id="6a032-318">Nustatykite parinkties **Dokumentų valdymas** reikšmę **Taip**, kaip parodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="6a032-318">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="6a032-319">**Pastaba.** Jei mobiliajame įrenginyje priedų rodyti nereikia, galite palikti nustatytą šios parinkties reikšmę **Ne**, kuri yra numatytasis nustatymas.</span><span class="sxs-lookup"><span data-stu-id="6a032-319">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
<span data-ttu-id="6a032-320">![Dokumentų tvarkymas](./media/docmanagement-216x300.png)</span><span class="sxs-lookup"><span data-stu-id="6a032-320">![Document management](./media/docmanagement-216x300.png)</span></span>
6.  <span data-ttu-id="6a032-321">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-321">Click **Done** to exit edit mode.</span></span>
7.  <span data-ttu-id="6a032-322">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-322">Click **Back** and then **Done** to exit the workspace</span></span>
8.  <span data-ttu-id="6a032-323">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="6a032-323">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="6a032-324">Tiekėjo SF eilutės paskirstymai</span><span class="sxs-lookup"><span data-stu-id="6a032-324">Vendor invoice line distributions</span></span>

<span data-ttu-id="6a032-325">Šio scenarijaus reikalavimai patvirtina, kad bus vykdomi tik eilutės lygio paskirstymai ir kad SF visada turės tik vieną eilutę.</span><span class="sxs-lookup"><span data-stu-id="6a032-325">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="6a032-326">Kadangi šis scenarijus yra paprastas, vartotojo patirtis mobiliajame įrenginyje taip pat turi būti pakankamai paprasta, kad paskirstymus norinčiam peržiūrėti vartotojui nereikėtų duomenų detalizuoti keliais lygiais.</span><span class="sxs-lookup"><span data-stu-id="6a032-326">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="6a032-327">„Finance and Operations“ tiekėjo SF apima galimybę rodyti visus sąskaitos faktūros antraštės paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="6a032-327">Vendor invoices in Finance and Operations include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="6a032-328">Ši patirtis yra tai, ko mums reikia mobiliajame scenarijuje.</span><span class="sxs-lookup"><span data-stu-id="6a032-328">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="6a032-329">Todėl norėdami kurti šią mobiliojo scenarijaus dalį naudosime puslapį **VendMobileInvoiceAllDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="6a032-329">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="6a032-330">Žinant reikalavimus galima lengviau nuspręsti, kurį konkretų puslapį naudoti ir kaip kuriant šį scenarijų optimizuoti vartotojo mobiliąją patirtį.</span><span class="sxs-lookup"><span data-stu-id="6a032-330">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="6a032-331">Antruoju scenarijumi paskirstymams rodyti naudosime kitą puslapį, nes to scenarijaus reikalavimai skiriasi.</span><span class="sxs-lookup"><span data-stu-id="6a032-331">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="6a032-332">URL pakeiskite meniu elemento pavadinimą, kaip tai padarėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="6a032-332">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="6a032-333">Pasirodžiusiame puslapyje turi būti tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="6a032-333">The page that appears should resemble the following illustration.</span></span>
<span data-ttu-id="6a032-334">[![Puslapis Visi paskirstymai](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="6a032-334">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>
2.  <span data-ttu-id="6a032-335">Atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6a032-335">Open the mobile designer from the **Settings** (gear) button.</span></span>
3.  <span data-ttu-id="6a032-336">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-336">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="6a032-337">**Pastaba.** Pastebėsite, kad automatiškai sukurti du nauji puslapiai.</span><span class="sxs-lookup"><span data-stu-id="6a032-337">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="6a032-338">Sistema šiuos puslapius kuria, ankstesniame skyriuje įjungėte dokumentų valdymo funkciją.</span><span class="sxs-lookup"><span data-stu-id="6a032-338">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="6a032-339">Šiuos naujus puslapius galite ignoruoti.</span><span class="sxs-lookup"><span data-stu-id="6a032-339">You can ignore these new pages.</span></span>
4.  <span data-ttu-id="6a032-340">Spustelėkite **Įtraukti puslapį**.</span><span class="sxs-lookup"><span data-stu-id="6a032-340">Click **Add page**.</span></span>
5.  <span data-ttu-id="6a032-341">Įveskite puslapio pavadinimą, pvz., **Apskaitos peržiūra**, ir aprašą, pvz., **SF apskaitos peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="6a032-341">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>
6.  <span data-ttu-id="6a032-342">Spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="6a032-342">Click **Done**.</span></span>
7.  <span data-ttu-id="6a032-343">Skirtuke **Laukai** spustelėkite **Pasirinkti laukus**, pasirinkite tolesnius laukus iš paskirstymų puslapio ir tada spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="6a032-343">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="6a032-344">Suma</span><span class="sxs-lookup"><span data-stu-id="6a032-344">Amount</span></span>
    2.  <span data-ttu-id="6a032-345">Valiuta</span><span class="sxs-lookup"><span data-stu-id="6a032-345">Currency</span></span>
    3.  <span data-ttu-id="6a032-346">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="6a032-346">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="6a032-347">Paskirstymų tinklelio stulpelio **Aprašas** nepasirinkome, nes šio scenarijaus reikalavimai patvirtino, kad išplėstinė kaina yra vienintelė suma, kuri bus paskirstyta.</span><span class="sxs-lookup"><span data-stu-id="6a032-347">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="6a032-348">Todėl paskirstymo sumos tipą norinčiam nustatyti vartotojui kito lauko nereikės.</span><span class="sxs-lookup"><span data-stu-id="6a032-348">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="6a032-349">Tačiau kitame scenarijuje mes **naudosime** šią informaciją, nes to scenarijaus reikalavimai nurodo, kad yra nustatytų kitų tipų sumų paskirstymų (pvz., PVM).</span><span class="sxs-lookup"><span data-stu-id="6a032-349">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>
8.  <span data-ttu-id="6a032-350">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-350">Click **Done** to exit edit mode.</span></span>
9.  <span data-ttu-id="6a032-351">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-351">Click **Back** and then **Done** to exit the workspace</span></span>
10. <span data-ttu-id="6a032-352">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="6a032-352">Click **Publish workspace** to save your work</span></span>

> [!NOTE] 
> <span data-ttu-id="6a032-353">Mobiliųjų įrenginių puslapis **Apskaitos peržiūra** nėra susietas su jokiais iki šiol sukurtais mobiliųjų įrenginių puslapiais.</span><span class="sxs-lookup"><span data-stu-id="6a032-353">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="6a032-354">Kadangi vartotojas privalo gebėti mobiliajame įrenginyje naršydamas iš puslapio **SF informacija** atidaryti puslapį **Apskaitos peržiūra**, turime pateikti nurodyti naršymą iš puslapio **SF informacija** į puslapį **Apskaitos peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="6a032-354">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="6a032-355">Šį naršymą nustatome naudodami papildomą logiką ir „JavaScript“.</span><span class="sxs-lookup"><span data-stu-id="6a032-355">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="6a032-356">Atidarykite anksčiau sukurtą .js failą ir įtraukite toliau nurodytu kodu pažymėtas eilutes.</span><span class="sxs-lookup"><span data-stu-id="6a032-356">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="6a032-357">Šio kodo paskirtys yra dvi.</span><span class="sxs-lookup"><span data-stu-id="6a032-357">This code does two things:</span></span>
    1.  <span data-ttu-id="6a032-358">Taip užtikrinama, kad naršydami puslapį **Apskaitos peržiūra** vartotojai negalės atidaryti darbo srities.</span><span class="sxs-lookup"><span data-stu-id="6a032-358">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="6a032-359">Sukuriamas naršymo iš puslapio **SF informacija** į puslapį **Apskaitos peržiūra** valdiklis.</span><span class="sxs-lookup"><span data-stu-id="6a032-359">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="6a032-360">Kode nurodyti puslapių ir kitų valdiklių pavadinimai turi sutapti su pavadinimais darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="6a032-360">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }

2.  <span data-ttu-id="6a032-361">Įkelkite kodo failą į darbo sritį pasirinkdami skirtuką **Logika**, kad perrašytumėte ankstesnį kodą</span><span class="sxs-lookup"><span data-stu-id="6a032-361">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="6a032-362">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="6a032-362">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="6a032-363">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="6a032-363">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="6a032-364">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="6a032-364">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="6a032-365">Tikrinimas</span><span class="sxs-lookup"><span data-stu-id="6a032-365">Validation</span></span>

<span data-ttu-id="6a032-366">Iš mobiliojo įrenginio atidarykite programą ir prijunkite ją prie savo „Finance and operations“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="6a032-366">From your mobile device, open the app, and connect to your Finance and Operations instance.</span></span> <span data-ttu-id="6a032-367">Įsitikinkite, kad prisijungėte prie įmonės, kurioje tiekėjo SF yra jums priskirtos peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="6a032-367">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="6a032-368">Turėtumėte galėti atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6a032-368">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="6a032-369">Peržiūrėti darbo sritį **Mano tvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="6a032-369">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="6a032-370">Detalizuoti darbo sritį **Mano tvirtinimai** ir peržiūrėti puslapį **Mano tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="6a032-370">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="6a032-371">Detalizuoti puslapį **Mano tiekėjo SF** ir peržiūrėti jums priskirtų SF sąrašą.</span><span class="sxs-lookup"><span data-stu-id="6a032-371">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="6a032-372">Detalizuoti vieną iš SF ir peržiūrėti SF antraštės ir eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="6a032-372">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="6a032-373">Informacijos puslapyje matyti saitą į priedus ir jį panaudojus atidaryti bei peržiūrėti priedų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="6a032-373">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="6a032-374">Informacijos puslapyje matyti saitą į puslapį **Apskaitos peržiūra** ir jį panaudojus atidaryti bei peržiūrėti paskirstymų puslapį.</span><span class="sxs-lookup"><span data-stu-id="6a032-374">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="6a032-375">Informacijos puslapio apačioje spustelėti meniu **Veiksmai** ir atlikti darbo eigos veiksmus, kurie taikomi darbo eigos veiksmui.</span><span class="sxs-lookup"><span data-stu-id="6a032-375">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="6a032-376">Fabrikam sudėtingo SF tvirtinimo scenarijaus kūrimas</span><span class="sxs-lookup"><span data-stu-id="6a032-376">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a032-377">Scenarijaus atributas</span><span class="sxs-lookup"><span data-stu-id="6a032-377">Scenario attribute</span></span></th>
<th><span data-ttu-id="6a032-378">Atsakymas</span><span class="sxs-lookup"><span data-stu-id="6a032-378">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a032-379">Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-379">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="6a032-380">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="6a032-380">Vendor name</span></span></li>
<li><span data-ttu-id="6a032-381">Iš viso su PVM</span><span class="sxs-lookup"><span data-stu-id="6a032-381">Invoice amount</span></span></li>
<li><span data-ttu-id="6a032-382">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="6a032-382">Invoice account</span></span></li>
<li><span data-ttu-id="6a032-383">SF numeris</span><span class="sxs-lookup"><span data-stu-id="6a032-383">Invoice number</span></span></li>
<li><span data-ttu-id="6a032-384">Data</span><span class="sxs-lookup"><span data-stu-id="6a032-384">Invoice date</span></span></li>
<li><span data-ttu-id="6a032-385">SF aprašas</span><span class="sxs-lookup"><span data-stu-id="6a032-385">Invoice description</span></span></li>
<li><span data-ttu-id="6a032-386">Terminas</span><span class="sxs-lookup"><span data-stu-id="6a032-386">Due date</span></span></li>
<li><span data-ttu-id="6a032-387">SF valiuta</span><span class="sxs-lookup"><span data-stu-id="6a032-387">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a032-388">Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-388">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="6a032-389">Įsigijimo kategorija</span><span class="sxs-lookup"><span data-stu-id="6a032-389">Procurement category</span></span></li>
<li><span data-ttu-id="6a032-390">Kiekis</span><span class="sxs-lookup"><span data-stu-id="6a032-390">Quantity</span></span></li>
<li><span data-ttu-id="6a032-391">Vnt. kaina</span><span class="sxs-lookup"><span data-stu-id="6a032-391">Unit price</span></span></li>
<li><span data-ttu-id="6a032-392">Grynoji eilutės suma</span><span class="sxs-lookup"><span data-stu-id="6a032-392">Line net amount</span></span></li>
<li><span data-ttu-id="6a032-393">1099 suma</span><span class="sxs-lookup"><span data-stu-id="6a032-393">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a032-394">Kiek SF yra SF eilučių?</span><span class="sxs-lookup"><span data-stu-id="6a032-394">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="6a032-395">Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</span><span class="sxs-lookup"><span data-stu-id="6a032-395">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="6a032-396">5</span><span class="sxs-lookup"><span data-stu-id="6a032-396">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a032-397">Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</span><span class="sxs-lookup"><span data-stu-id="6a032-397">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="6a032-398">Taip</span><span class="sxs-lookup"><span data-stu-id="6a032-398">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a032-399">Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos ir t. t.)?</span><span class="sxs-lookup"><span data-stu-id="6a032-399">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="6a032-400">Vėl taikykite 80 / 20 taisyklę.</span><span class="sxs-lookup"><span data-stu-id="6a032-400">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="6a032-401">Išplėstinė kaina: 2 PVM: 2 Išlaidos: 2</span><span class="sxs-lookup"><span data-stu-id="6a032-401">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a032-402">Ar SF antraštėje taip pat yra apskaitos paskirstymų?</span><span class="sxs-lookup"><span data-stu-id="6a032-402">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="6a032-403">Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="6a032-403">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="6a032-404">Nenaudojama</span><span class="sxs-lookup"><span data-stu-id="6a032-404">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a032-405">Ar vartotojai įrenginyje norės matyti SF priedus?</span><span class="sxs-lookup"><span data-stu-id="6a032-405">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="6a032-406">Taip</span><span class="sxs-lookup"><span data-stu-id="6a032-406">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="6a032-407">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="6a032-407">Next steps</span></span>

<span data-ttu-id="6a032-408">Galima vykdyti tolesnius 1 scenarijaus variantus, atsižvelgiant į 2 scenarijaus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="6a032-408">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="6a032-409">Šį skyrių galite naudoti norėdami patobulinti mobiliosios programos patirtį.</span><span class="sxs-lookup"><span data-stu-id="6a032-409">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="6a032-410">Kadangi 2 scenarijuje galima tikėtis daugiau SF eilučių, toliau nurodyti dizaino keitimai padės optimizuoti vartotojo patirtį mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="6a032-410">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="6a032-411">Vartotojai gali pasirinkti peržiūrėti SF eilutes atskirame mobiliųjų įrenginių puslapyje, o ne informacijos puslapyje (1 scenarijaus atveju).</span><span class="sxs-lookup"><span data-stu-id="6a032-411">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="6a032-412">Kadangi šiame scenarijuje galima tikėtis daugiau SF eilučių, jei puslapis **VendMobileInvoiceAllDistributionTree** naudojamas mobiliųjų įrenginių paskirstymų puslapiui kurti (1 scenarijaus atveju), vartotojas gali nesuprasti, kaip eilutes susieti su paskirstymais.</span><span class="sxs-lookup"><span data-stu-id="6a032-412">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="6a032-413">Todėl paskirstymų puslapiui kurti naudokite puslapį **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="6a032-413">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="6a032-414">Geriausia šiame scenarijuje būtų paskirstymus rodyti SF eilutės kontekste.</span><span class="sxs-lookup"><span data-stu-id="6a032-414">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="6a032-415">Todėl įsitikinkite, kad vartotojas gali detalizuoti eilutę ir peržiūrėti paskirstymų puslapį.</span><span class="sxs-lookup"><span data-stu-id="6a032-415">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="6a032-416">Naudokite puslapio saito galimybę, kad nustatytumėte detalizavimo funkciją (kaip tai atlikote 1 scenarijuje nustatydami antraštės ir informacijos puslapių detalizavimo funkciją).</span><span class="sxs-lookup"><span data-stu-id="6a032-416">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="6a032-417">Kadangi 2 scenarijuje tikimasi daugiau nei vieno tipo sumos paskirstymų (PVM, išlaidos ir t. t.), būtų naudinga parodyti sumos tipo aprašą.</span><span class="sxs-lookup"><span data-stu-id="6a032-417">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="6a032-418">(1 scenarijuje šia informaciją praleidome.)</span><span class="sxs-lookup"><span data-stu-id="6a032-418">(We omitted this information in scenario 1.)</span></span>





