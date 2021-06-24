---
title: SF patvirtinimai mobiliąja programa
description: Šioje temoje pateikiamas praktinis mobiliųjų įrenginių scenarijų kūrimo metodas, pavyzdyje naudojant tiekėjo SF tvirtinimus mobiliuosiuose įrenginiuose.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 78ab17952801a1d77f321e212bb61e9b45d93216
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189207"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="00b09-103">SF patvirtinimai mobiliąja programa</span><span class="sxs-lookup"><span data-stu-id="00b09-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00b09-104">Mobiliųjų įrenginių galimybės verslo vartotojui suteikia galimybę kurti mobiliąją patirtį.</span><span class="sxs-lookup"><span data-stu-id="00b09-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="00b09-105">Sudėtingesniais scenarijais platforma taip pat suteikia galimybę kūrėjams pagal poreikį galimybes išplėsti.</span><span class="sxs-lookup"><span data-stu-id="00b09-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="00b09-106">Efektyviausias būdas susipažinti su kai kuriomis naujomis mobiliųjų įrenginių sąvokomis yra peržiūrėti kelių scenarijų kūrimo procesą.</span><span class="sxs-lookup"><span data-stu-id="00b09-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="00b09-107">Šioje temoje pateikiamas praktinis mobiliųjų įrenginių scenarijų kūrimo metodas, pavyzdyje naudojant tiekėjo SF tvirtinimus mobiliuosiuose įrenginiuose.</span><span class="sxs-lookup"><span data-stu-id="00b09-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="00b09-108">Ši tema turėtų padėti sukurti kitus scenarijų variantus ir pritaikyti žinias kitiems scenarijams, kurie nėra susiję su tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="00b09-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="00b09-109">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="00b09-109">Prerequisites</span></span>

| <span data-ttu-id="00b09-110">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="00b09-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="00b09-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="00b09-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00b09-112">Išankstinis mobiliųjų įrenginių vadovo perskaitymas</span><span class="sxs-lookup"><span data-stu-id="00b09-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="00b09-113">Mobilioji platforma</span><span class="sxs-lookup"><span data-stu-id="00b09-113">Mobile platform</span></span>](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="00b09-114">„Dynamics 365 Finance“</span><span class="sxs-lookup"><span data-stu-id="00b09-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="00b09-115">Aplinka, kurioje yra 1611 versija ir 3 platformos naujinimas (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="00b09-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="00b09-116">Įdiekite karštąsias pataisas KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="00b09-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="00b09-117">Užduočių įrašymo priemonė gali klaidingai įrašyti dvi išplečiamųjų dialogų komandas Uždaryti; tai įtraukta į 3 platformos naujinį (2016 m. lapkričio mėn. naujinys).</span><span class="sxs-lookup"><span data-stu-id="00b09-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="00b09-118">Įdiekite karštąsias pataisas KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="00b09-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="00b09-119">Įdiegus šias karštąsias pataisas, priedus galima peržiūrėti mobiliajame kliente; tai įtraukta į 3 platformos naujinį (2016 m. lapkričio mėn. naujinys).</span><span class="sxs-lookup"><span data-stu-id="00b09-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="00b09-120">Įdiekite karštąsias pataisas KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="00b09-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="00b09-121">Tiekėjo SF mobiliuosiuose įrenginiuose tvirtinimo programos kodas; tai įtraukta į 7.0.1 programos versiją (2016 m. gegužės mėn.).</span><span class="sxs-lookup"><span data-stu-id="00b09-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="00b09-122">„Android“, „iOS“ arba „Windows“ įrenginys, kuriame įdiegta mobilioji programa.</span><span class="sxs-lookup"><span data-stu-id="00b09-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="00b09-123">Ieškokite programos atitinkamoje programų parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="00b09-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="00b09-124">Įžanga</span><span class="sxs-lookup"><span data-stu-id="00b09-124">Introduction</span></span>
<span data-ttu-id="00b09-125">Norint tiekėjo SF tvirtinti mobiliuosiuose įrenginiuose, reikia įdiegti tris karštąsias pataisas, paminėtas skyriuje „Būtinosios sąlygos“.</span><span class="sxs-lookup"><span data-stu-id="00b09-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="00b09-126">Šios karštosios pataisos nepateikia SF tvirtinimo darbo srities.</span><span class="sxs-lookup"><span data-stu-id="00b09-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="00b09-127">Norėdami sužinoti, kas yra darbo sritis mobiliųjų įrenginių kontekste, perskaitykite mobiliųjų įrenginių vadovą, paminėtą skyriuje „Būtinosios sąlygos“.</span><span class="sxs-lookup"><span data-stu-id="00b09-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="00b09-128">SF tvirtinimo darbo sritį reikia sukurti.</span><span class="sxs-lookup"><span data-stu-id="00b09-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="00b09-129">Kiekviena organizacija skirtingai planuoja ir nustato tiekėjo SF verslo procesą.</span><span class="sxs-lookup"><span data-stu-id="00b09-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="00b09-130">Prieš kurdami tiekėjo SF tvirtinimo mobiliuosiuose įrenginiuose patirtį, atsižvelkite į toliau nurodytus verslo proceso aspektus.</span><span class="sxs-lookup"><span data-stu-id="00b09-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="00b09-131">Tikslas yra kiek įmanoma labiau naudoti šiuos duomenų taškus ir optimizuoti vartotojo patirtį mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="00b09-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="00b09-132">Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="00b09-133">Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="00b09-134">Kiek SF yra SF eilučių?</span><span class="sxs-lookup"><span data-stu-id="00b09-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="00b09-135">Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</span><span class="sxs-lookup"><span data-stu-id="00b09-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="00b09-136">Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</span><span class="sxs-lookup"><span data-stu-id="00b09-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="00b09-137">Jei atsakymas į šį klausimą yra teigiamas, atsižvelkite į tolesnius klausimus.</span><span class="sxs-lookup"><span data-stu-id="00b09-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="00b09-138">Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos, skaidymai ir t. t.)?</span><span class="sxs-lookup"><span data-stu-id="00b09-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="00b09-139">Vėl taikykite 80 / 20 taisyklę.</span><span class="sxs-lookup"><span data-stu-id="00b09-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="00b09-140">Ar SF antraštėje taip pat yra apskaitos paskirstymų?</span><span class="sxs-lookup"><span data-stu-id="00b09-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="00b09-141">Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="00b09-142">Šioje temoje nepaaiškinama, kaip redaguoti apskaitos paskirstymus, nes mobiliųjų įrenginių scenarijuose ši funkcija šiuo metu nepalaikoma.</span><span class="sxs-lookup"><span data-stu-id="00b09-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="00b09-143">Ar vartotojai įrenginyje norės matyti SF priedus?</span><span class="sxs-lookup"><span data-stu-id="00b09-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="00b09-144">SF tvirtinimo mobiliuosiuose įrenginiuose patirties kūrimas skirsis, priklausomai nuo atsakymų į šiuos klausimus.</span><span class="sxs-lookup"><span data-stu-id="00b09-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="00b09-145">Tikslas yra optimizuoti organizacijos verslo proceso valdymo mobiliuosiuose įrenginiuose vartotojo patirtį.</span><span class="sxs-lookup"><span data-stu-id="00b09-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="00b09-146">Likusioje šios temos dalyje peržiūrėsime du scenarijų variantus, kurie pagrįsti skirtingais atsakymais į ankstesnius klausimus.</span><span class="sxs-lookup"><span data-stu-id="00b09-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="00b09-147">Paprastai dirbant su mobiliųjų įrenginių dizaino įrankiu patariama nepamiršti publikuoti keitimų, kad neprarastumėte naujinimų.</span><span class="sxs-lookup"><span data-stu-id="00b09-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="00b09-148">Paprasto sąskaitos faktūros patvirtinimo scenarijaus kūrimas „Contoso”</span><span class="sxs-lookup"><span data-stu-id="00b09-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00b09-149">Scenarijaus atributas</span><span class="sxs-lookup"><span data-stu-id="00b09-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="00b09-150">Atsakymas</span><span class="sxs-lookup"><span data-stu-id="00b09-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00b09-151">Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="00b09-152">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="00b09-152">Vendor name</span></span></li>
<li><span data-ttu-id="00b09-153">Bendroji SF suma</span><span class="sxs-lookup"><span data-stu-id="00b09-153">Invoice total</span></span></li>
<li><span data-ttu-id="00b09-154">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="00b09-154">Invoice account</span></span></li>
<li><span data-ttu-id="00b09-155">SF numeris</span><span class="sxs-lookup"><span data-stu-id="00b09-155">Invoice number</span></span></li>
<li><span data-ttu-id="00b09-156">Data</span><span class="sxs-lookup"><span data-stu-id="00b09-156">Invoice date</span></span></li>
<li><span data-ttu-id="00b09-157">SF aprašas</span><span class="sxs-lookup"><span data-stu-id="00b09-157">Invoice description</span></span></li>
<li><span data-ttu-id="00b09-158">Terminas</span><span class="sxs-lookup"><span data-stu-id="00b09-158">Due date</span></span></li>
<li><span data-ttu-id="00b09-159">SF valiuta</span><span class="sxs-lookup"><span data-stu-id="00b09-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00b09-160">Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="00b09-161">Įsigijimo kategorija</span><span class="sxs-lookup"><span data-stu-id="00b09-161">Procurement category</span></span></li>
<li><span data-ttu-id="00b09-162">Kiekis</span><span class="sxs-lookup"><span data-stu-id="00b09-162">Quantity</span></span></li>
<li><span data-ttu-id="00b09-163">Vnt. kaina</span><span class="sxs-lookup"><span data-stu-id="00b09-163">Unit price</span></span></li>
<li><span data-ttu-id="00b09-164">Grynoji eilutės suma</span><span class="sxs-lookup"><span data-stu-id="00b09-164">Line net amount</span></span></li>
<li><span data-ttu-id="00b09-165">1099 suma</span><span class="sxs-lookup"><span data-stu-id="00b09-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00b09-166">Kiek SF yra SF eilučių?</span><span class="sxs-lookup"><span data-stu-id="00b09-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="00b09-167">Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</span><span class="sxs-lookup"><span data-stu-id="00b09-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="00b09-168">1</span><span class="sxs-lookup"><span data-stu-id="00b09-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00b09-169">Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</span><span class="sxs-lookup"><span data-stu-id="00b09-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="00b09-170">Taip</span><span class="sxs-lookup"><span data-stu-id="00b09-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00b09-171">Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos ir t. t.)?</span><span class="sxs-lookup"><span data-stu-id="00b09-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="00b09-172">Vėl taikykite 80 / 20 taisyklę.</span><span class="sxs-lookup"><span data-stu-id="00b09-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="00b09-173">Išplėstinė kaina: 2 PVM: 0 Išlaidos: 0</span><span class="sxs-lookup"><span data-stu-id="00b09-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00b09-174">Ar SF antraštėje taip pat yra apskaitos paskirstymų?</span><span class="sxs-lookup"><span data-stu-id="00b09-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="00b09-175">Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="00b09-176">Nenaudojama</span><span class="sxs-lookup"><span data-stu-id="00b09-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00b09-177">Ar vartotojai įrenginyje norės matyti SF priedus?</span><span class="sxs-lookup"><span data-stu-id="00b09-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="00b09-178">Taip</span><span class="sxs-lookup"><span data-stu-id="00b09-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="00b09-179">Darbo srities kūrimas</span><span class="sxs-lookup"><span data-stu-id="00b09-179">Create the workspace</span></span>

1.  <span data-ttu-id="00b09-180">Naršyklėje ir prisijunkite prie programos.</span><span class="sxs-lookup"><span data-stu-id="00b09-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="00b09-181">Prisijungę pridėkite dalį **&mode=mobile** prie URL, kaip parodyta tolesniame pavyzdyje, ir atnaujinkite puslapį: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="00b09-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="00b09-182">Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**.</span><span class="sxs-lookup"><span data-stu-id="00b09-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="00b09-183">Mobiliųjų programų dizaino įrankis pasirodo taip, kaip pasirodo užduočių įrašymo priemonė.</span><span class="sxs-lookup"><span data-stu-id="00b09-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="00b09-184">Spustelėkite **Įtraukti**, kad sukurtumėte naują darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="00b09-185">Šiuo atveju darbo sritį pavadinkite **Mano tvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="00b09-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="00b09-186">Įvesti aprašymą.</span><span class="sxs-lookup"><span data-stu-id="00b09-186">Enter a description.</span></span>
6.  <span data-ttu-id="00b09-187">Pasirinkti darbo srities spalvą.</span><span class="sxs-lookup"><span data-stu-id="00b09-187">Select a workspace color.</span></span> <span data-ttu-id="00b09-188">Darbo srities spalva bus naudojama bendram šios darbo srities mobiliosios patirties stiliui kurti.</span><span class="sxs-lookup"><span data-stu-id="00b09-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="00b09-189">Pasirinkite darbo srities piktogramą.</span><span class="sxs-lookup"><span data-stu-id="00b09-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="00b09-190">Spustelėkite **Atlikta**</span><span class="sxs-lookup"><span data-stu-id="00b09-190">Click **Done**</span></span>
9.  <span data-ttu-id="00b09-191">Spustelėkite **Publikuoti darbo sritį**, kad išsaugotumėte keitimus</span><span class="sxs-lookup"><span data-stu-id="00b09-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="00b09-192">Man priskirtos tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="00b09-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="00b09-193">Pirmasis mobiliųjų įrenginių puslapis, kurį turėtumėte sukurti, yra SF, kurios priskirtos vartotojui peržiūrėti, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="00b09-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="00b09-194">Norėdami kurti šį mobiliųjų įrenginių puslapį, naudokite puslapį **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="00b09-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="00b09-195">Prieš baigdami šią procedūrą įsitikinkite, kad bent viena tiekėjo SF yra jums priskirta peržiūrėti ir kad SF eilutėje yra du paskirstymai.</span><span class="sxs-lookup"><span data-stu-id="00b09-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="00b09-196">Ši sąranka atitinka šio scenarijaus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="00b09-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="00b09-197">URL pakeiskite meniu elemento pavadinimą į **VendMobileInvoiceAssignedToMeListPage**, kad atidarytumėte sąrašo puslapio **Man priskirtos laukiančios tiekėjo SF** mobiliąją versiją modulyje **Mokėtinos sumos**.</span><span class="sxs-lookup"><span data-stu-id="00b09-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="00b09-198">Atsižvelgiant į SF, kurios jūsų sistemoje jums priskirtos, skaičių, šiame puslapyje bus rodomos tos SF.</span><span class="sxs-lookup"><span data-stu-id="00b09-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="00b09-199">Norėdami rasi konkrečią SF, galite naudoti dešinėje pusėje pateiktą filtrą.</span><span class="sxs-lookup"><span data-stu-id="00b09-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="00b09-200">Tačiau šiame pavyzdyje konkreti SF nėra reikalinga.</span><span class="sxs-lookup"><span data-stu-id="00b09-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="00b09-201">Tereikia, kad jums būtų priskirta kokia nors SF, jog galėtumėte kurti mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="00b09-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="00b09-202">Nauji puslapiai, kuriuos galima naudoti, buvo specialiai sukurti tiekėjo SF mobiliųjų įrenginių scenarijams kurti.</span><span class="sxs-lookup"><span data-stu-id="00b09-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="00b09-203">Todėl turite šiuos puslapius naudoti.</span><span class="sxs-lookup"><span data-stu-id="00b09-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="00b09-204">URL turėtų būti toks, kaip toliau, ir įvedus URL turi būti rodomas puslapis su iliustracija: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="00b09-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="00b09-205">[![Puslapis Laukiama man priskirtų tiekėjo SF](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="00b09-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="00b09-206">Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**</span><span class="sxs-lookup"><span data-stu-id="00b09-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="00b09-207">Pasirinkite savo darbo sritį ir spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="00b09-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="00b09-208">Spustelėkite **Įtraukti puslapį**, kad sukurtumėte pirmą mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="00b09-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="00b09-209">Įveskite pavadinimą, pvz., **Mano tiekėjo SF**, ir aprašą, pvz., **Man peržiūrėti priskirtos tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="00b09-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="00b09-210">Spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="00b09-210">Click **Done**.</span></span>
7.  <span data-ttu-id="00b09-211">Mobiliųjų įrenginių dizaino įrankio skirtuke **Laukai** spustelėkite **Pasirinkti laukus**.</span><span class="sxs-lookup"><span data-stu-id="00b09-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="00b09-212">Šio sąrašo puslapio stulpeliuose turi būti tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="00b09-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="00b09-213">[![Stulpeliai puslapyje Man priskirtos laukiančios tiekėjo SF](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="00b09-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="00b09-214">Iš sąrašo puslapio įtraukite reikiamus stulpelius, kurie vartotojams turi būti rodomi mobiliųjų įrenginių puslapyje.</span><span class="sxs-lookup"><span data-stu-id="00b09-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="00b09-215">Galutiniam vartotojui laukai bus rodomi ta tvarka, kuria juos įtrauksite.</span><span class="sxs-lookup"><span data-stu-id="00b09-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="00b09-216">Laukų tvarką galima pakeisti tik iš naujo pažymint visus laukus.</span><span class="sxs-lookup"><span data-stu-id="00b09-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="00b09-217">Pagal šio scenarijaus reikalavimus reikalingi aštuoni toliau nurodyti laukai.</span><span class="sxs-lookup"><span data-stu-id="00b09-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="00b09-218">Tačiau kai kuriems vartotojams aštuoni laukai gali pasirodyti per didelis informacijos kiekis mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="00b09-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="00b09-219">Todėl mobiliųjų įrenginių sąrašo rodinyje bus rodomi tik patys svarbiausi laukai.</span><span class="sxs-lookup"><span data-stu-id="00b09-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="00b09-220">Likę laukai bus rodomi informacijos rodinyje, kurį sukursime vėliau.</span><span class="sxs-lookup"><span data-stu-id="00b09-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="00b09-221">Dabar įtrauksime toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="00b09-221">For now, we will add the following fields.</span></span> <span data-ttu-id="00b09-222">Spustelėkite šių stulpelių pliuso ženklą (**+**), kad įtrauktumėte į mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="00b09-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="00b09-223">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="00b09-223">Vendor name</span></span>
    - <span data-ttu-id="00b09-224">Bendroji SF suma</span><span class="sxs-lookup"><span data-stu-id="00b09-224">Invoice total</span></span>
    - <span data-ttu-id="00b09-225">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="00b09-225">Invoice account</span></span>
    - <span data-ttu-id="00b09-226">SF numeris</span><span class="sxs-lookup"><span data-stu-id="00b09-226">Invoice number</span></span>
    - <span data-ttu-id="00b09-227">Data</span><span class="sxs-lookup"><span data-stu-id="00b09-227">Invoice date</span></span>

    <span data-ttu-id="00b09-228">Įvedus laukus mobiliųjų įrenginių puslapyje turi būti rodoma tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="00b09-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="00b09-229">[![Puslapio rodinys įtraukus laukus](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="00b09-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="00b09-230">Taip pat dabar turite įtraukti tolesnius stulpelius, kad vėliau galėtumėte įjungti darbo eigos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00b09-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="00b09-231">Rodyti baigti užduotį</span><span class="sxs-lookup"><span data-stu-id="00b09-231">Show complete task</span></span>
    - <span data-ttu-id="00b09-232">Rodyti perduoti užduotį</span><span class="sxs-lookup"><span data-stu-id="00b09-232">Show delegate task</span></span>
    - <span data-ttu-id="00b09-233">Rodyti atšaukti užduotį</span><span class="sxs-lookup"><span data-stu-id="00b09-233">Show recall task</span></span>
    - <span data-ttu-id="00b09-234">Rodyti atmesti užduotį</span><span class="sxs-lookup"><span data-stu-id="00b09-234">Show reject task</span></span>
    - <span data-ttu-id="00b09-235">Rodyti prašyti užpildymo užduoties</span><span class="sxs-lookup"><span data-stu-id="00b09-235">Show request completion task</span></span>
    - <span data-ttu-id="00b09-236">Rodyti iš naujo pateikti užduotį</span><span class="sxs-lookup"><span data-stu-id="00b09-236">Show resubmit task</span></span>

10. <span data-ttu-id="00b09-237">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="00b09-238">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="00b09-239">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą.</span><span class="sxs-lookup"><span data-stu-id="00b09-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="00b09-240">Mokėtinų sumų parametrų formoje, prie dalies **SF** įjunkite parinktį **Laukiančių tiekėjo SF sąraše rodyti bendrą SF sumą**.</span><span class="sxs-lookup"><span data-stu-id="00b09-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="00b09-241">Atminkite, kad tik įjungus šį parametrą SF sumos bus apskaičiuotos ir rodomos laukiančių tiekėjo SF sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="00b09-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="00b09-242">Ši nauja galimybė yra būtinų karštųjų pataisų 3208224 dalis.</span><span class="sxs-lookup"><span data-stu-id="00b09-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="00b09-243">Tiekėjo SF informacija</span><span class="sxs-lookup"><span data-stu-id="00b09-243">Vendor invoice details</span></span>

<span data-ttu-id="00b09-244">Norėdami kurti sąskaitų faktūrų informacijos mobiliųjų įrenginių puslapį, naudokite puslapį **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="00b09-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="00b09-245">Atminkite, kad, atsižvelgiant į SF, kurios sistemoje jums priskirtos, skaičių, šiame puslapyje rodoma seniausia SF (SF, kuri buvo sukurta pirmoji).</span><span class="sxs-lookup"><span data-stu-id="00b09-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="00b09-246">Norėdami rasi konkrečią SF, galite naudoti dešinėje pusėje pateiktą filtrą.</span><span class="sxs-lookup"><span data-stu-id="00b09-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="00b09-247">Tačiau šiame pavyzdyje konkreti SF nėra reikalinga.</span><span class="sxs-lookup"><span data-stu-id="00b09-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="00b09-248">Tereikia kokių nors SF duomenų, kad galėtumėte kurti mobiliųjų įrenginių puslapį.</span><span class="sxs-lookup"><span data-stu-id="00b09-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="00b09-249">[![Darbo eigos puslapis](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="00b09-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="00b09-250">URL pakeiskite meniu elemento pavadinimą įrašydami **VendMobileInvoiceHeaderDetails**, kad atidarytumėte formą</span><span class="sxs-lookup"><span data-stu-id="00b09-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="00b09-251">Atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="00b09-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="00b09-252">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="00b09-253">Pasirinkite puslapį **Mano tiekėjo SF**, kurį sukūrėte anksčiau, tada spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="00b09-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="00b09-254">Skirtuke **Laukai** spustelėkite stulpelio antraštę **Tinklelis**.</span><span class="sxs-lookup"><span data-stu-id="00b09-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="00b09-255">Spustelėkite **Ypatybės &gt; Įtraukti puslapį**.</span><span class="sxs-lookup"><span data-stu-id="00b09-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="00b09-256">**Pastaba.** Kai spustelėjate antraštę **Tinklelis** ir įtraukiate puslapį, ryšys su informacijos puslapiu nustatomas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="00b09-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="00b09-257">Įveskite puslapio pavadinimą, pvz., **SF informacija SF**, ir aprašą, pvz., **SF antraštės ir eilutės informacijos peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="00b09-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="00b09-258">Spustelėkite **Pasirinkti laukus**.</span><span class="sxs-lookup"><span data-stu-id="00b09-258">Click **Select fields**.</span></span> <span data-ttu-id="00b09-259">Atminkite, kad galutiniam vartotojui laukai bus rodomi ta tvarka, kuria juos įtrauksite.</span><span class="sxs-lookup"><span data-stu-id="00b09-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="00b09-260">Laukų tvarką galima pakeisti tik iš naujo pažymint visus laukus.</span><span class="sxs-lookup"><span data-stu-id="00b09-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="00b09-261">Iš antraštės įtraukite toliau nurodytus laukus, atsižvelgdami į šio scenarijaus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="00b09-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="00b09-262">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="00b09-262">Vendor name</span></span>
   - <span data-ttu-id="00b09-263">Bendroji SF suma</span><span class="sxs-lookup"><span data-stu-id="00b09-263">Invoice total</span></span>
   - <span data-ttu-id="00b09-264">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="00b09-264">Invoice account</span></span>
   - <span data-ttu-id="00b09-265">SF numeris</span><span class="sxs-lookup"><span data-stu-id="00b09-265">Invoice number</span></span>
   - <span data-ttu-id="00b09-266">Data</span><span class="sxs-lookup"><span data-stu-id="00b09-266">Invoice date</span></span>
   - <span data-ttu-id="00b09-267">SF aprašas</span><span class="sxs-lookup"><span data-stu-id="00b09-267">Invoice description</span></span>
   - <span data-ttu-id="00b09-268">Terminas</span><span class="sxs-lookup"><span data-stu-id="00b09-268">Due date</span></span>
   - <span data-ttu-id="00b09-269">SF valiuta</span><span class="sxs-lookup"><span data-stu-id="00b09-269">Invoice currency</span></span>

10. <span data-ttu-id="00b09-270">Iš puslapio eilučių tinklelio įtraukite toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="00b09-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="00b09-271">Įsigijimo kategorija</span><span class="sxs-lookup"><span data-stu-id="00b09-271">Procurement category</span></span>
    - <span data-ttu-id="00b09-272">Kiekis</span><span class="sxs-lookup"><span data-stu-id="00b09-272">Quantity</span></span>
    - <span data-ttu-id="00b09-273">Vnt. kaina</span><span class="sxs-lookup"><span data-stu-id="00b09-273">Unit price</span></span>
    - <span data-ttu-id="00b09-274">Grynoji eilutės suma</span><span class="sxs-lookup"><span data-stu-id="00b09-274">Line net amount</span></span>
    - <span data-ttu-id="00b09-275">1099 suma</span><span class="sxs-lookup"><span data-stu-id="00b09-275">1099 amount</span></span>

11. <span data-ttu-id="00b09-276">Kai visi ankstesniuose dviejuose veiksmuose nurodyti laukai įtraukti, spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="00b09-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="00b09-277">Puslapyje turi būti tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="00b09-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="00b09-278">[![Iliustracija, rodanti įtrauktus papildomus laukus](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="00b09-278">[![Illustration showing additional fields added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="00b09-279">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="00b09-280">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="00b09-281">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="00b09-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="00b09-282">Darbo eigos veiksmai</span><span class="sxs-lookup"><span data-stu-id="00b09-282">Workflow actions</span></span>

<span data-ttu-id="00b09-283">Norėdami įtraukti darbo eigos veiksmų, naudokite puslapį **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="00b09-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="00b09-284">Norėdami atidaryti šį puslapį, URL pakeiskite meniu elemento pavadinimą, kaip tai padarėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="00b09-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="00b09-285">Tada atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="00b09-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="00b09-286">Norėdami į informacijos puslapį įtraukti darbo eigos veiksmų, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00b09-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="00b09-287">Jums turi būti priskirta tam tikrą būseną turinčių sąskaitų faktūrų, jog kurdami galėtumėte naudoti darbo eigos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00b09-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="00b09-288">Darbo eigos veiksmų įrašymas</span><span class="sxs-lookup"><span data-stu-id="00b09-288">Record workflow actions</span></span>
1.  <span data-ttu-id="00b09-289">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="00b09-290">Pasirinkite puslapį **SF informacija**, kurį sukūrėte anksčiau, o tada spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="00b09-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="00b09-291">Skirtuke **Veiksmai** spustelėkite **Įtraukti veiksmą**.</span><span class="sxs-lookup"><span data-stu-id="00b09-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="00b09-292">Įveskite veiksmo pavadinimą, pvz., **Tvirtinti**, tada įveskite aprašymą, pvz., **Tvirtinti SF**.</span><span class="sxs-lookup"><span data-stu-id="00b09-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="00b09-293">Atkreipkite dėmesį, kad čia įvestas veiksmo pavadinimas tampa mobiliojoje programoje vartotojui rodomo veiksmo pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="00b09-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="00b09-294">Spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="00b09-294">Click **Done**.</span></span>
6.  <span data-ttu-id="00b09-295">Spustelėkite **Pasirinkti laukus**.</span><span class="sxs-lookup"><span data-stu-id="00b09-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="00b09-296">Atidarykite darbo eigos procesą puslapyje **VendMobileInvoiceHeaderDetails** ir užbaikite veiksmą, kurį norėjote įrašyti.</span><span class="sxs-lookup"><span data-stu-id="00b09-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="00b09-297">Įsitikinkite, kad šio proceso metu įvedėte darbo eigos komentarus, kad į mobiliąją patirtį taip pat būtų įtrauktas komentarų laukas.</span><span class="sxs-lookup"><span data-stu-id="00b09-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="00b09-298">Paleidę darbo eigos veiksmą, spustelėkite **Atlikta**, kad baigtumėte užduoti Pasirinkti laukus.</span><span class="sxs-lookup"><span data-stu-id="00b09-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="00b09-299">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="00b09-300">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="00b09-301">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="00b09-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="00b09-302">Pakartodami ankstesnius veiksmus įrašykite visus reikiamus darbo eigos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00b09-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="00b09-303">.js failo kūrimas</span><span class="sxs-lookup"><span data-stu-id="00b09-303">Create a .js file</span></span>
1. <span data-ttu-id="00b09-304">Atidarykite „Notepad“ arba „Microsoft Visual Studio“ ir įklijuokite tolesnį kodą.</span><span class="sxs-lookup"><span data-stu-id="00b09-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="00b09-305">Įrašykite failą kaip .js failą.</span><span class="sxs-lookup"><span data-stu-id="00b09-305">Save the file as a .js file.</span></span> <span data-ttu-id="00b09-306">Šis kodas atlieka šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="00b09-306">This code does the following:</span></span>
    - <span data-ttu-id="00b09-307">Jis paslepia papildomus su darbo eiga susijusius stulpelius, kuriuos į mobiliųjų įrenginių sąrašo puslapį mes įtraukėme anksčiau.</span><span class="sxs-lookup"><span data-stu-id="00b09-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="00b09-308">Šiuos stulpelius mes įtraukėme, kad programai pateiktume informacijos kontekstą ir ji galėtų atlikti kitą veiksmą.</span><span class="sxs-lookup"><span data-stu-id="00b09-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="00b09-309">Atsižvelgiant į aktyvų darbo eigos veiksmą, jis pritaiko logiką, kad būtų rodomi tik tie veiksmai.</span><span class="sxs-lookup"><span data-stu-id="00b09-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="00b09-310">Kode nurodyti puslapių ir kitų valdiklių pavadinimai turi sutapti su pavadinimais darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="00b09-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
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
    ```

2.  <span data-ttu-id="00b09-311">Įkelkite kodo failą į darbo sritį pasirinkdami skirtuką **Logika**</span><span class="sxs-lookup"><span data-stu-id="00b09-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="00b09-312">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="00b09-313">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="00b09-314">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="00b09-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="00b09-315">Tiekėjo SF priedai</span><span class="sxs-lookup"><span data-stu-id="00b09-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="00b09-316">Spustelėkite viršutiniame dešiniajame puslapio kampe esantį (krumpliaračio) mygtuką **Parametrai“** ir tada spustelėkite **Mobilioji programa**</span><span class="sxs-lookup"><span data-stu-id="00b09-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="00b09-317">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="00b09-318">Pasirinkite puslapį <strong>SF informacija, \*\*kurį sukūrėte anksčiau, o tada spustelėkite \*\*Redaguoti</strong>.</span><span class="sxs-lookup"><span data-stu-id="00b09-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="00b09-319">Nustatykite parinkties **Dokumentų valdymas** reikšmę **Taip**, kaip parodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="00b09-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="00b09-320">**Pastaba.** Jei mobiliajame įrenginyje priedų rodyti nereikia, galite palikti nustatytą šios parinkties reikšmę **Ne**, kuri yra numatytasis nustatymas.</span><span class="sxs-lookup"><span data-stu-id="00b09-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Dokumentų tvarkymas](./media/docmanagement-216x300.png)

5. <span data-ttu-id="00b09-322">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="00b09-323">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="00b09-324">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="00b09-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="00b09-325">Tiekėjo SF eilutės paskirstymai</span><span class="sxs-lookup"><span data-stu-id="00b09-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="00b09-326">Šio scenarijaus reikalavimai patvirtina, kad bus vykdomi tik eilutės lygio paskirstymai ir kad SF visada turės tik vieną eilutę.</span><span class="sxs-lookup"><span data-stu-id="00b09-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="00b09-327">Kadangi šis scenarijus yra paprastas, vartotojo patirtis mobiliajame įrenginyje taip pat turi būti pakankamai paprasta, kad paskirstymus norinčiam peržiūrėti vartotojui nereikėtų duomenų detalizuoti keliais lygiais.</span><span class="sxs-lookup"><span data-stu-id="00b09-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="00b09-328">Tiekėjo SF apima galimybę rodyti visus sąskaitos faktūros antraštės paskirstymus.</span><span class="sxs-lookup"><span data-stu-id="00b09-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="00b09-329">Ši patirtis yra tai, ko mums reikia mobiliajame scenarijuje.</span><span class="sxs-lookup"><span data-stu-id="00b09-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="00b09-330">Todėl norėdami kurti šią mobiliojo scenarijaus dalį naudosime puslapį **VendMobileInvoiceAllDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="00b09-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="00b09-331">Žinant reikalavimus galima lengviau nuspręsti, kurį konkretų puslapį naudoti ir kaip kuriant šį scenarijų optimizuoti vartotojo mobiliąją patirtį.</span><span class="sxs-lookup"><span data-stu-id="00b09-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="00b09-332">Antruoju scenarijumi paskirstymams rodyti naudosime kitą puslapį, nes to scenarijaus reikalavimai skiriasi.</span><span class="sxs-lookup"><span data-stu-id="00b09-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="00b09-333">URL pakeiskite meniu elemento pavadinimą, kaip tai padarėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="00b09-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="00b09-334">Pasirodžiusiame puslapyje turi būti tolesnėje iliustracijoje nurodyta informacija.</span><span class="sxs-lookup"><span data-stu-id="00b09-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="00b09-335">[![Puslapis Visi paskirstymai](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="00b09-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="00b09-336">Atidarykite mobiliųjų įrenginių dizaino įrankį spustelėdami (krumpliaračio) mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="00b09-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="00b09-337">Spustelėkite mygtuką **Redaguoti**, kad įjungtumėte darbo srities redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="00b09-338">**Pastaba.** Pastebėsite, kad automatiškai sukurti du nauji puslapiai.</span><span class="sxs-lookup"><span data-stu-id="00b09-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="00b09-339">Sistema šiuos puslapius kuria, ankstesniame skyriuje įjungėte dokumentų valdymo funkciją.</span><span class="sxs-lookup"><span data-stu-id="00b09-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="00b09-340">Šiuos naujus puslapius galite ignoruoti.</span><span class="sxs-lookup"><span data-stu-id="00b09-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="00b09-341">Spustelėkite **Įtraukti puslapį**.</span><span class="sxs-lookup"><span data-stu-id="00b09-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="00b09-342">Įveskite puslapio pavadinimą, pvz., **Apskaitos peržiūra**, ir aprašą, pvz., **SF apskaitos peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="00b09-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="00b09-343">Spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="00b09-343">Click **Done**.</span></span>

7.  <span data-ttu-id="00b09-344">Skirtuke **Laukai** spustelėkite **Pasirinkti laukus**, pasirinkite tolesnius laukus iš paskirstymų puslapio ir tada spustelėkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="00b09-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="00b09-345">Suma</span><span class="sxs-lookup"><span data-stu-id="00b09-345">Amount</span></span>
    2.  <span data-ttu-id="00b09-346">Valiuta</span><span class="sxs-lookup"><span data-stu-id="00b09-346">Currency</span></span>
    3.  <span data-ttu-id="00b09-347">DK sąskaita</span><span class="sxs-lookup"><span data-stu-id="00b09-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="00b09-348">Paskirstymų tinklelio stulpelio **Aprašas** nepasirinkome, nes šio scenarijaus reikalavimai patvirtino, kad išplėstinė kaina yra vienintelė suma, kuri bus paskirstyta.</span><span class="sxs-lookup"><span data-stu-id="00b09-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="00b09-349">Todėl paskirstymo sumos tipą norinčiam nustatyti vartotojui kito lauko nereikės.</span><span class="sxs-lookup"><span data-stu-id="00b09-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="00b09-350">Tačiau kitame scenarijuje mes **naudosime** šią informaciją, nes to scenarijaus reikalavimai nurodo, kad yra nustatytų kitų tipų sumų paskirstymų (pvz., PVM).</span><span class="sxs-lookup"><span data-stu-id="00b09-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="00b09-351">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="00b09-352">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="00b09-353">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="00b09-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="00b09-354">Naršymo įtraukimas į puslapį Apskaitos peržiūra</span><span class="sxs-lookup"><span data-stu-id="00b09-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="00b09-355">Mobiliųjų įrenginių puslapis **Apskaitos peržiūra** nėra susietas su jokiais iki šiol sukurtais mobiliųjų įrenginių puslapiais.</span><span class="sxs-lookup"><span data-stu-id="00b09-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="00b09-356">Kadangi vartotojas privalo gebėti mobiliajame įrenginyje naršydamas iš puslapio **SF informacija** atidaryti puslapį **Apskaitos peržiūra**, turime pateikti nurodyti naršymą iš puslapio **SF informacija** į puslapį **Apskaitos peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="00b09-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="00b09-357">Šį naršymą nustatome naudodami papildomą logiką ir „JavaScript“.</span><span class="sxs-lookup"><span data-stu-id="00b09-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="00b09-358">Atidarykite anksčiau sukurtą .js failą ir įtraukite toliau nurodytu kodu pažymėtas eilutes.</span><span class="sxs-lookup"><span data-stu-id="00b09-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="00b09-359">Šio kodo paskirtys yra dvi.</span><span class="sxs-lookup"><span data-stu-id="00b09-359">This code does two things:</span></span>
    1.  <span data-ttu-id="00b09-360">Taip užtikrinama, kad naršydami puslapį **Apskaitos peržiūra** vartotojai negalės atidaryti darbo srities.</span><span class="sxs-lookup"><span data-stu-id="00b09-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="00b09-361">Sukuriamas naršymo iš puslapio **SF informacija** į puslapį **Apskaitos peržiūra** valdiklis.</span><span class="sxs-lookup"><span data-stu-id="00b09-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="00b09-362">Kode nurodyti puslapių ir kitų valdiklių pavadinimai turi sutapti su pavadinimais darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="00b09-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
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
    ```
    
2.  <span data-ttu-id="00b09-363">Įkelkite kodo failą į darbo sritį pasirinkdami skirtuką **Logika**, kad perrašytumėte ankstesnį kodą</span><span class="sxs-lookup"><span data-stu-id="00b09-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="00b09-364">Spustelėkite **Atlikta**, kad uždarytumėte redagavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="00b09-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="00b09-365">Spustelėkite **Atgal** ir tada spustelėkite **baigta**, kad uždarytumėte darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="00b09-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="00b09-366">Spustelėkite **Publikuoti darbo sritį**, kad įrašytumėte savo darbą</span><span class="sxs-lookup"><span data-stu-id="00b09-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="00b09-367">Tikrinimas</span><span class="sxs-lookup"><span data-stu-id="00b09-367">Validation</span></span>

<span data-ttu-id="00b09-368">Iš mobiliojo įrenginio atidarykite programą ir prisijunkite prie egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="00b09-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="00b09-369">Įsitikinkite, kad prisijungėte prie įmonės, kurioje tiekėjo SF yra jums priskirtos peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="00b09-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="00b09-370">Turėtumėte galėti atlikti tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00b09-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="00b09-371">Peržiūrėti darbo sritį **Mano tvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="00b09-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="00b09-372">Detalizuoti darbo sritį **Mano tvirtinimai** ir peržiūrėti puslapį **Mano tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="00b09-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="00b09-373">Detalizuoti puslapį **Mano tiekėjo SF** ir peržiūrėti jums priskirtų SF sąrašą.</span><span class="sxs-lookup"><span data-stu-id="00b09-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="00b09-374">Detalizuoti vieną iš SF ir peržiūrėti SF antraštės ir eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="00b09-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="00b09-375">Informacijos puslapyje matyti saitą į priedus ir jį panaudojus atidaryti bei peržiūrėti priedų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="00b09-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="00b09-376">Informacijos puslapyje matyti saitą į puslapį **Apskaitos peržiūra** ir jį panaudojus atidaryti bei peržiūrėti paskirstymų puslapį.</span><span class="sxs-lookup"><span data-stu-id="00b09-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="00b09-377">Informacijos puslapio apačioje spustelėti meniu **Veiksmai** ir atlikti darbo eigos veiksmus, kurie taikomi darbo eigos veiksmui.</span><span class="sxs-lookup"><span data-stu-id="00b09-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="00b09-378">Fabrikam sudėtingo SF tvirtinimo scenarijaus kūrimas</span><span class="sxs-lookup"><span data-stu-id="00b09-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00b09-379">Scenarijaus atributas</span><span class="sxs-lookup"><span data-stu-id="00b09-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="00b09-380">Atsakymas</span><span class="sxs-lookup"><span data-stu-id="00b09-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00b09-381">Kokius SF antraštės laukus (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="00b09-382">Tiekėjo vardas</span><span class="sxs-lookup"><span data-stu-id="00b09-382">Vendor name</span></span></li>
<li><span data-ttu-id="00b09-383">Iš viso su PVM</span><span class="sxs-lookup"><span data-stu-id="00b09-383">Invoice amount</span></span></li>
<li><span data-ttu-id="00b09-384">Mokėtojo kodas</span><span class="sxs-lookup"><span data-stu-id="00b09-384">Invoice account</span></span></li>
<li><span data-ttu-id="00b09-385">SF numeris</span><span class="sxs-lookup"><span data-stu-id="00b09-385">Invoice number</span></span></li>
<li><span data-ttu-id="00b09-386">Data</span><span class="sxs-lookup"><span data-stu-id="00b09-386">Invoice date</span></span></li>
<li><span data-ttu-id="00b09-387">SF aprašas</span><span class="sxs-lookup"><span data-stu-id="00b09-387">Invoice description</span></span></li>
<li><span data-ttu-id="00b09-388">Terminas</span><span class="sxs-lookup"><span data-stu-id="00b09-388">Due date</span></span></li>
<li><span data-ttu-id="00b09-389">SF valiuta</span><span class="sxs-lookup"><span data-stu-id="00b09-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00b09-390">Kokias SF antraštės eilutes (ir kokia tvarka) vartotojas norės matyti mobiliajame įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="00b09-391">Įsigijimo kategorija</span><span class="sxs-lookup"><span data-stu-id="00b09-391">Procurement category</span></span></li>
<li><span data-ttu-id="00b09-392">Kiekis</span><span class="sxs-lookup"><span data-stu-id="00b09-392">Quantity</span></span></li>
<li><span data-ttu-id="00b09-393">Vnt. kaina</span><span class="sxs-lookup"><span data-stu-id="00b09-393">Unit price</span></span></li>
<li><span data-ttu-id="00b09-394">Grynoji eilutės suma</span><span class="sxs-lookup"><span data-stu-id="00b09-394">Line net amount</span></span></li>
<li><span data-ttu-id="00b09-395">1099 suma</span><span class="sxs-lookup"><span data-stu-id="00b09-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00b09-396">Kiek SF yra SF eilučių?</span><span class="sxs-lookup"><span data-stu-id="00b09-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="00b09-397">Čia taikykite 80 / 20 taisyklę ir optimizuokite 80 proc.</span><span class="sxs-lookup"><span data-stu-id="00b09-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="00b09-398">5</span><span class="sxs-lookup"><span data-stu-id="00b09-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00b09-399">Ar mobiliuosiuose įrenginiuose peržiūros metu vartotojai norės matyti apskaitos paskirstymą (SF kodavimą)?</span><span class="sxs-lookup"><span data-stu-id="00b09-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="00b09-400">Taip</span><span class="sxs-lookup"><span data-stu-id="00b09-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00b09-401">Kiek SF eilutėje yra apskaitos paskirstymų (išplėstinė kaina, PVM, išlaidos ir t. t.)?</span><span class="sxs-lookup"><span data-stu-id="00b09-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="00b09-402">Vėl taikykite 80 / 20 taisyklę.</span><span class="sxs-lookup"><span data-stu-id="00b09-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="00b09-403">Išplėstinė kaina: 2 PVM: 2 Išlaidos: 2</span><span class="sxs-lookup"><span data-stu-id="00b09-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00b09-404">Ar SF antraštėje taip pat yra apskaitos paskirstymų?</span><span class="sxs-lookup"><span data-stu-id="00b09-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="00b09-405">Jei taip, ar šie apskaitos paskirstymai turėtų būti pasiekiami įrenginyje?</span><span class="sxs-lookup"><span data-stu-id="00b09-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="00b09-406">Nenaudojama</span><span class="sxs-lookup"><span data-stu-id="00b09-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00b09-407">Ar vartotojai įrenginyje norės matyti SF priedus?</span><span class="sxs-lookup"><span data-stu-id="00b09-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="00b09-408">Taip</span><span class="sxs-lookup"><span data-stu-id="00b09-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="00b09-409">Kiti veiksmai</span><span class="sxs-lookup"><span data-stu-id="00b09-409">Next steps</span></span>

<span data-ttu-id="00b09-410">Galima vykdyti tolesnius 1 scenarijaus variantus, atsižvelgiant į 2 scenarijaus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="00b09-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="00b09-411">Šį skyrių galite naudoti norėdami patobulinti mobiliosios programos patirtį.</span><span class="sxs-lookup"><span data-stu-id="00b09-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="00b09-412">Kadangi 2 scenarijuje galima tikėtis daugiau SF eilučių, toliau nurodyti dizaino keitimai padės optimizuoti vartotojo patirtį mobiliajame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="00b09-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="00b09-413">Vartotojai gali pasirinkti peržiūrėti SF eilutes atskirame mobiliųjų įrenginių puslapyje, o ne informacijos puslapyje (1 scenarijaus atveju).</span><span class="sxs-lookup"><span data-stu-id="00b09-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="00b09-414">Kadangi šiame scenarijuje galima tikėtis daugiau SF eilučių, jei puslapis **VendMobileInvoiceAllDistributionTree** naudojamas mobiliųjų įrenginių paskirstymų puslapiui kurti (1 scenarijaus atveju), vartotojas gali nesuprasti, kaip eilutes susieti su paskirstymais.</span><span class="sxs-lookup"><span data-stu-id="00b09-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="00b09-415">Todėl paskirstymų puslapiui kurti naudokite puslapį **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="00b09-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="00b09-416">Geriausia šiame scenarijuje būtų paskirstymus rodyti SF eilutės kontekste.</span><span class="sxs-lookup"><span data-stu-id="00b09-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="00b09-417">Todėl įsitikinkite, kad vartotojas gali detalizuoti eilutę ir peržiūrėti paskirstymų puslapį.</span><span class="sxs-lookup"><span data-stu-id="00b09-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="00b09-418">Naudokite puslapio saito galimybę, kad nustatytumėte detalizavimo funkciją (kaip tai atlikote 1 scenarijuje nustatydami antraštės ir informacijos puslapių detalizavimo funkciją).</span><span class="sxs-lookup"><span data-stu-id="00b09-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="00b09-419">Kadangi 2 scenarijuje tikimasi daugiau nei vieno tipo sumos paskirstymų (PVM, išlaidos ir t. t.), būtų naudinga parodyti sumos tipo aprašą.</span><span class="sxs-lookup"><span data-stu-id="00b09-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="00b09-420">(1 scenarijuje šia informaciją praleidome.)</span><span class="sxs-lookup"><span data-stu-id="00b09-420">(We omitted this information in scenario 1.)</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
