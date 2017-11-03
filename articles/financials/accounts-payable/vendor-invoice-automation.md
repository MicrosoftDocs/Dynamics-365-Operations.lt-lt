---
title: "Tiekėjo sąskaitų faktūrų automatizavimas"
description: "Šioje temoje paaiškinamos funkcijos, pasiekiamos iki galo automatizuojant tiekėjų SF – net ir SF su priedais."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 00de566dcfbd3eb8c72816f66599863fa6cd1a41
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="vendor-invoice-automation"></a><span data-ttu-id="3a8eb-103">Tiekėjo sąskaitų faktūrų automatizavimas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-103">Vendor invoice automation</span></span>

<span data-ttu-id="3a8eb-104">Šioje temoje paaiškinamos funkcijos, pasiekiamos iki galo automatizuojant tiekėjų SF – net ir SF su priedais.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-104">This topic explains the features that are available for end-to-end automation of vendor invoices, even invoices that include attachments.</span></span>

<span data-ttu-id="3a8eb-105">Organizacijos, kurios nori supaprastinti savo mokėtinų sumų (AP) procesus, dažnai identifikuoja SF apdorojimą kaip vieną iš svarbiausių proceso sričių, kuri turi būti efektyvesnė.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-105">Organizations that want to streamline their Accounts payable (AP) processes often identify invoice processing as one of the top process areas that should be more efficient.</span></span> <span data-ttu-id="3a8eb-106">Daugeliu atvejų šios organizacijos popierinių SF apdorojimą perduoda trečiųjų šalių optinio ženklų atpažinimo (OCR) paslaugų teikėjui.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-106">In many cases, these organizations offload the processing of paper invoices to a third-party optical character recognition (OCR) service provider.</span></span> <span data-ttu-id="3a8eb-107">Tada jie gauna SF metaduomenis, kuriuos galima perskaityti kompiuteriu, kartu su nuskaitytu kiekvienos SF vaizdu.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-107">They then receive machine-readable invoice metadata together with a scanned image of each invoice.</span></span> <span data-ttu-id="3a8eb-108">Siekiant padėti automatizuoti sukuriamas „paskutinės mylios“ sprendimas, kad būtų galima panaudoti šiuos artefaktus SF išrašymo sistemoje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-108">To help with automation, a “last mile” solution is then built to enable consumption of these artifacts in the invoicing system.</span></span> <span data-ttu-id="3a8eb-109">„Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimas, dabar standartiškai suteikia šį „paskutinės mylios“ automatizavimą su SF automatizavimo sprendimu.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-109">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition now enables this “last mile” automation out of the box, through an invoice automation solution.</span></span>

## <a name="solution-context"></a><span data-ttu-id="3a8eb-110">Sprendimo kontekstas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-110">Solution context</span></span>

<span data-ttu-id="3a8eb-111">SF automatizavimo sprendimas suteikia standartinę sąsają, kuri gali priimti SF antraštės ir eilučių metaduomenis bei SF priedus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-111">The invoice automation solution enables a standard interface that can accept invoice metadata for the invoice header and invoice lines, and also attachments that are applicable to the invoice.</span></span> <span data-ttu-id="3a8eb-112">Bet kokia išorinė sistema, kuri gali sugeneruoti artefaktus, atitinkančius šią sąsają, galės siųsti informacijos santrauką į „Finance and Operations“, kad būtų galima automatiškai apdoroti SF ir priedus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-112">Any external system that can generate artifacts that comply with this interface will be able to send the feed into Finance and Operations for automatic processing of invoices and attachments.</span></span>

<span data-ttu-id="3a8eb-113">Pateiktame paveikslėlyje parodytas integravimo scenarijaus pavyzdys, kuriame „Contoso“ bendradarbiauja su OCR paslaugų tiekėju dėl tiekėjo SF apdorojimo.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-113">The following illustration shows a sample integration scenario where Contoso has partnered with an OCR service provider for vendor invoice processing.</span></span> <span data-ttu-id="3a8eb-114">„Contoso“ tiekėjai siunčia SF paslaugų teikėjui el. paštu.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-114">Contoso’s vendors send invoices to the service provider by email.</span></span> <span data-ttu-id="3a8eb-115">Naudodamas OCR apdorojimą paslaugų teikėjas sugeneruoja SF metaduomenis (antraštė ir / arba eilutės) ir nuskaito SF vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-115">Through OCR processing, the service provider generates invoice metadata (header and/or lines) and a scanned image of the invoice.</span></span> <span data-ttu-id="3a8eb-116">Tada integravimo sluoksnis transformuoja šiuos artefaktus taip, kad „Finance and Operations“ galėtų juos naudoti.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-116">An integration layer then transforms these artifacts so that Finance and Operations can consume them.</span></span>

![Integravimo scenarijaus pavyzdys](media/vendor_invoice_automation_01.png)

<span data-ttu-id="3a8eb-118">Jei būtinas SF integravimas, galimi keli anksčiau nurodyto scenarijaus variantai.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-118">Several variations of the preceding scenario are possible if invoice integration is required.</span></span> <span data-ttu-id="3a8eb-119">Duomenų perkėlimas yra kitas naudojimo atvejis, kai ši sąsaja gali būti naudojama norint sukurti „Finance and Operations“ SF ir priedus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-119">Data migration is another use case where this interface can be used to create invoices and attachments in Finance and Operations.</span></span>

### <a name="solution-components"></a><span data-ttu-id="3a8eb-120">Sprendimo komponentai</span><span class="sxs-lookup"><span data-stu-id="3a8eb-120">Solution components</span></span>

<span data-ttu-id="3a8eb-121">Sprendimo pagrindą sudaro šie komponentai:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-121">The solution footprint consists of the following components:</span></span>

+ <span data-ttu-id="3a8eb-122">SF antraštės, SF eilučių ir SF priedų duomenų objektai</span><span class="sxs-lookup"><span data-stu-id="3a8eb-122">Data entities for the invoice header, invoice lines, and invoice attachments</span></span>
+ <span data-ttu-id="3a8eb-123">SF išimčių apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-123">Exception processing for invoices</span></span>
+ <span data-ttu-id="3a8eb-124">SF priedų peržiūros vienas šalia kito žiūryklė</span><span class="sxs-lookup"><span data-stu-id="3a8eb-124">A side-by-side attachment viewer in invoices</span></span>

<span data-ttu-id="3a8eb-125">Likusioje šios temos dalyje pateikiami išsamūs šių sprendimų komponentų aprašai.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-125">The rest of this topic provides detailed descriptions of these solution components.</span></span>

## <a name="data-entities"></a><span data-ttu-id="3a8eb-126">Duomenų objektai</span><span class="sxs-lookup"><span data-stu-id="3a8eb-126">Data entities</span></span>

<span data-ttu-id="3a8eb-127">Duomenų paketas yra darbo vienetas, kuris turi būti išsiųstas į „Finance and Operations“, kad būtų galima sukurti SF antraštes, SF eilutes ir SF priedus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-127">A data package is the unit of work that must be sent to Finance and Operations, so that invoice headers, invoice lines, and invoice attachments can be created.</span></span> <span data-ttu-id="3a8eb-128">Šie duomenų objektai naudojami artefaktams, kurie sudaro duomenų paketą:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-128">The following data entities are used for the artifacts that make up the data package:</span></span>

+ <span data-ttu-id="3a8eb-129">Tiekėjo SF antraštė</span><span class="sxs-lookup"><span data-stu-id="3a8eb-129">Vendor invoice header</span></span>
+ <span data-ttu-id="3a8eb-130">Tiekėjo SF eilutė</span><span class="sxs-lookup"><span data-stu-id="3a8eb-130">Vendor invoice line</span></span>
+ <span data-ttu-id="3a8eb-131">Tiekėjo SF dokumento priedas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-131">Vendor invoice document attachment</span></span>

<span data-ttu-id="3a8eb-132">Tiekėjo SF dokumento priedas yra naujas duomenų objektas, pristatomas kaip šios funkcijos dalis.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-132">Vendor invoice document attachment is a new data entity that is introduced as part of this feature.</span></span> <span data-ttu-id="3a8eb-133">Tiekėjo SF antraštės objektas buvo pakeistas, kad palaikytų priedus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-133">The Vendor invoice header entity has been modified so that it supports attachments.</span></span> <span data-ttu-id="3a8eb-134">Tiekėjo SF eilutės objektas nebuvo modifikuotas šioje funkcijoje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-134">The Vendor invoice line entity hasn’t been modified for this feature.</span></span>

<span data-ttu-id="3a8eb-135">Šioje temoje nėra išsamaus duomenų paketo apibrėžimo.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-135">This topic doesn’t give a detailed definition of a data package.</span></span> <span data-ttu-id="3a8eb-136">Joje taip pat nepaaiškinta, kaip sukurti duomenų paketus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-136">It also doesn’t explain how to create data packages.</span></span> <span data-ttu-id="3a8eb-137">Šią informaciją rasite [Duomenų objektų ir paketų sistema](../../dev-itpro/data-entities/data-entities-data-packages.md).</span><span class="sxs-lookup"><span data-stu-id="3a8eb-137">For this information, see [Data entities and packages framework](../../dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

<span data-ttu-id="3a8eb-138">Norėdami greitai sugeneruoti bandymo duomenis, kurie apima SF ir priedus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-138">To quickly generate test data that includes invoices and attachments, follow these steps.</span></span>

1. <span data-ttu-id="3a8eb-139">Prisijunkite prie savo „Finance and Operations“ egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-139">Sign in to your Finance and Operations instance.</span></span>
1. <span data-ttu-id="3a8eb-140">Eikite į **Mokėtinos sumos** > **SF** > **Laukiančios tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-140">Go to **Accounts payables** > **Invoices** > **Pending vendor invoices**.</span></span>
1. <span data-ttu-id="3a8eb-141">Sukurkite SF, kuriose yra eilučių ir priedų.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-141">Create invoices that have lines and attachments.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a8eb-142">Priedai turi būti antraštės priedai.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-142">The attachments must be header attachments.</span></span> <span data-ttu-id="3a8eb-143">Šiuo metu tiekėjo SF dokumento priedo objektas nepalaiko eilučių priedų.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-143">Currently, the Vendor invoice document attachment entity doesn’t support line attachments.</span></span>

1. <span data-ttu-id="3a8eb-144">Atidarykite darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-144">Open the **Data management** workspace.</span></span>
1. <span data-ttu-id="3a8eb-145">Sukurkite eksportavimo užduotį, kurioje yra tiekėjo SF antraštė, tiekėjo SF eilutė ir tiekėjo SF dokumento priedų objektų.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-145">Create an export job that includes the Vendor invoice header, Vendor invoice line, and Vendor invoice document attachment entities.</span></span>
1. <span data-ttu-id="3a8eb-146">Eksportuokite duomenis.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-146">Export the data.</span></span>
1. <span data-ttu-id="3a8eb-147">Atsisiųskite eksportuotus duomenis kaip paketą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-147">Download the exported data as a package.</span></span> <span data-ttu-id="3a8eb-148">Dabar galite naudoti paketą norėdami importuoti duomenis į paskirties egzempliorius bandymo tikslais.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-148">You can now use the package to import data into target instances for testing purposes.</span></span>

### <a name="determining-the-legal-entity-for-an-invoice"></a><span data-ttu-id="3a8eb-149">SF juridinio subjekto nustatymas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-149">Determining the legal entity for an invoice</span></span>

<span data-ttu-id="3a8eb-150">SF, importuotas naudojant duomenų paketus, galima susieti su juridiniu subjektu, kuriam jos priklauso dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-150">Invoices that are imported via data packages can be associated with the legal entity that they belong to in two ways:</span></span>

+ <span data-ttu-id="3a8eb-151">Importavimo užduotis, kuri apdoroja SF, importuoja ją į tą pačią įmonę, kurioje užduotis buvo suplanuota **Duomenų valdymo** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-151">The import job that processes the invoice imports it into the same company in which the job was scheduled in the **Data management** workspace.</span></span> <span data-ttu-id="3a8eb-152">Kitaip sakant, užduoties įmonė nustato įmonę, kuriai priklauso SF.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-152">In other words, the company of the job determines the company that the invoice belongs to.</span></span>
+ <span data-ttu-id="3a8eb-153">Kai duomenų paketas, kuriame yra SF, išsiunčiamas į „Finance and Operations“, kvietyklė (t. y. integracijos programa, kuri veikia ne programoje „Finance and Operations“) gali aiškiai nurodyti įmonės ID HTTP užklausoje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-153">When the data package that contains invoices is sent to Finance and Operations, the caller (that is, the integration application that runs outside of Finance and Operations) can explicitly mention the company ID in the HTTP request.</span></span> <span data-ttu-id="3a8eb-154">Šiuo atveju nepaisoma įmonės konteksto, kuriame vykdoma apdorojimo užduotis programoje „Finance and Operations“, ir SF importuojamos į įmonę, kuri perduoda naudojant HTTP užklausą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-154">In this case, the company context in which the processing job runs in Finance and Operations is overridden, and the invoices are imported into the company that was passed via the HTTP request.</span></span>

> [!NOTE]
> <span data-ttu-id="3a8eb-155">Šis veikimas yra standartinis duomenų valdymo veikimas.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-155">This behavior is standard data management behavior.</span></span> <span data-ttu-id="3a8eb-156">Kalbant apie SF tai paaiškinta dėl išsamumo.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-156">It’s explained here, in the context of invoices, just for the sake of completeness.</span></span>

## <a name="exception-processing"></a><span data-ttu-id="3a8eb-157">Išimties apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-157">Exception processing</span></span>

<span data-ttu-id="3a8eb-158">Tokiais atvejais, kai tiekėjo SF pasiekia „Finance and Operations“ naudojant integraciją, mokėtinų sumų komandos narys turi galėti lengvai apdoroti nesėkmingų SF išimtis ir iš tokių SF sukurti laukiančias SF.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-158">In scenarios where vendor invoices come into Finance and Operations via integration, there must be an easy way for an Accounts payable team member to process exceptions or failed invoices, and to create pending invoices out of failed invoices.</span></span> <span data-ttu-id="3a8eb-159">Šis tiekėjo SF išimčių apdorojimas dabar yra „Finance and Operations“ dalis.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-159">This exception processing for vendor invoices is now part of Finance and Operations.</span></span>

### <a name="exceptions-list-page"></a><span data-ttu-id="3a8eb-160">Išimčių sąrašo puslapis</span><span class="sxs-lookup"><span data-stu-id="3a8eb-160">Exceptions list page</span></span>

<span data-ttu-id="3a8eb-161">Naujas SF išimčių sąrašo puslapis yra pasiekiamas atsidarius **Mokėtinos sumos** > **SF** > **Importavimo triktys** > **Tiekėjo SF, kurių nepavyko importuoti**.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-161">The new list page for invoice exceptions is available at **Accounts payable** > **Invoices** > **Import failures** > **Vendor invoices that failed to import**.</span></span> <span data-ttu-id="3a8eb-162">Šiame puslapyje rodomi visi tiekėjo SF antraščių įrašai iš tiekėjo SF antraščių duomenų objekto išdėstymo lentelės.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-162">This page shows all the vendor invoice header records from the staging table of the Vendor invoice header data entity.</span></span> <span data-ttu-id="3a8eb-163">Atkreipkite dėmesį, kad tuos pačius įrašus galite peržiūrėti iš **Duomenų valdymo** darbo srities, kurioje galite atlikti tuos pačius veiksmus, kurie pateikiami išimčių tvarkymo funkcijoje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-163">Note that you can view the same records from the **Data management** workspace, where you can also perform the same actions that are provided in the exception handling feature.</span></span> <span data-ttu-id="3a8eb-164">Tačiau UI, kurią pateikia išimčių tvarkymo funkcija, yra optimizuota funkciniam vartotojui.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-164">However, the UI that the exception handling feature provides is optimized for a functional user.</span></span>

![Išimčių sąrašo puslapis](media/vendor_invoice_automation_02.png)

<span data-ttu-id="3a8eb-166">Šiame sąrašo puslapyje yra tokie laukai, gaunami naudojant informacijos santrauką:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-166">This list page includes the following fields that come in via the feed:</span></span>

+ <span data-ttu-id="3a8eb-167">**Įmonė** – įmonė, kuriai priklauso SF</span><span class="sxs-lookup"><span data-stu-id="3a8eb-167">**Company** – The company that the invoice belongs to</span></span>
+ <span data-ttu-id="3a8eb-168">**Klaidos pranešimas** – klaidos pranešimas, kurį duomenų valdymo sistema išleidžia, kad paaiškintų, kodėl nepavyko sukurti SF</span><span class="sxs-lookup"><span data-stu-id="3a8eb-168">**Error message** – The error message that the data management framework issues to explain why the invoice could not be created</span></span>
+ <span data-ttu-id="3a8eb-169">**Numeris** – SF numeris</span><span class="sxs-lookup"><span data-stu-id="3a8eb-169">**Number** – The invoice number</span></span>
+ <span data-ttu-id="3a8eb-170">**SF kodas**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-170">**Invoice account**</span></span>
+ <span data-ttu-id="3a8eb-171">**Pavadinimas** – tiekėjo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-171">**Name** – The vendor’s name</span></span>
+ <span data-ttu-id="3a8eb-172">**Tiekėjo sąskaita**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-172">**Vendor account**</span></span>
+ <span data-ttu-id="3a8eb-173">**Pirkimo užsakymas** – SF pirkimo užsakymo (PO) numeris</span><span class="sxs-lookup"><span data-stu-id="3a8eb-173">**Purchase order** – The purchase order (PO) number for the invoice</span></span>
+ <span data-ttu-id="3a8eb-174">**Registravimo data**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-174">**Posting date**</span></span>
+ <span data-ttu-id="3a8eb-175">**SF data**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-175">**Invoice date**</span></span>
+ <span data-ttu-id="3a8eb-176">**SF aprašas**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-176">**Invoice description**</span></span>
+ <span data-ttu-id="3a8eb-177">**Valiuta**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-177">**Currency**</span></span>
+ <span data-ttu-id="3a8eb-178">**Žurnalas**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-178">**Log**</span></span>
+ <span data-ttu-id="3a8eb-179">**Eilutės nuoroda** – identifikatorius, gaunamas iš išorinės sistemos</span><span class="sxs-lookup"><span data-stu-id="3a8eb-179">**Line reference** – The identifier that comes from the external system</span></span>

    > [!NOTE]
    > <span data-ttu-id="3a8eb-180">Eilutės nuoroda nėra SF ID.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-180">The line reference isn’t the invoice ID.</span></span>

<span data-ttu-id="3a8eb-181">Šiame sąrašo puslapyje taip pat yra peržiūros sritis, kurią galite naudoti šiais būdais:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-181">This list page also has a preview pane that you can used in the following ways:</span></span>

+ <span data-ttu-id="3a8eb-182">Peržiūrėkite visą klaidos pranešimą, kad stulpelio **Klaidos pranešimas** nereikėtų išplėsti tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-182">View the whole error message, so that you don’t have to expand the **Error message** column in the grid.</span></span>
+ <span data-ttu-id="3a8eb-183">Peržiūrėkite visą SF priedų sąrašą, jei su SF gauta kokių nors priedų.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-183">View the whole list of attachments for the invoice, if any attachments came with the invoice.</span></span>

<span data-ttu-id="3a8eb-184">Sąrašo puslapis palaiko šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-184">The list page supports the following actions:</span></span>

+ <span data-ttu-id="3a8eb-185">**Redaguoti** – atidarykite išimties įrašą redagavimo režimu, kad būtų galima išspręsti problemas.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-185">**Edit** – Open the exception record in edit mode, so that you can fix the issues.</span></span>
+ <span data-ttu-id="3a8eb-186">**Parinktys** – pasiekite standartines parinktis, esančias sąrašo puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-186">**Options** – Access the standard options that are available on list pages.</span></span> <span data-ttu-id="3a8eb-187">Galite naudoti parinktį **Įtraukti į darbo sritį** norėdami prisegti išimčių sąrašo puslapį prie darbo srities kaip sąrašą arba plytelę.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-187">You can use the **Add to workspace** option to pin the exceptions list page to your workspace as a list or tile.</span></span>

### <a name="exception-details-page"></a><span data-ttu-id="3a8eb-188">Išimčių informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="3a8eb-188">Exception details page</span></span>

<span data-ttu-id="3a8eb-189">Paleidus redagavimo režimą, rodomas SF, kurioje yra problemų, išimčių informacijos puslapis.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-189">When you start edit mode, the exception details page for the invoice that has issues appears.</span></span> <span data-ttu-id="3a8eb-190">Jei yra kokių nors priedų, SF ir numatytasis priedas išimčių informacijos puslapyje rodomi vienas šalia kito.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-190">If there are any attachments, the invoice and the default attachment appear side by side on the exception details page.</span></span>

![Išimčių informacijos puslapis](media/vendor_invoice_automation_03.png)

<span data-ttu-id="3a8eb-192">Ankstesniame paveikslėlyje nėra jokių gautos tiekėjo SF antraštės eilučių.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-192">In the preceding illustration, there weren’t any lines for the vendor invoice header that came in.</span></span> <span data-ttu-id="3a8eb-193">Todėl eilučių skyrius yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-193">Therefore, the lines section is empty.</span></span>

<span data-ttu-id="3a8eb-194">Išimčių informacijos puslapis palaiko šią operaciją:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-194">The exception details page supports the following operation:</span></span>

+ <span data-ttu-id="3a8eb-195">**Kurti laukiančią SF** – kai apdorodami išimtis išsprendžiate SF problemas, galite spustelėti šį mygtuką, kad sukurtumėte laukiančią SF.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-195">**Create pending invoice** – After you’ve fixed the issues on the invoice as part of exception processing, you can click this button to create the pending invoice.</span></span> <span data-ttu-id="3a8eb-196">Laukiančios SF kuriamos fone (kaip nesinchroninė operacija).</span><span class="sxs-lookup"><span data-stu-id="3a8eb-196">The creation of pending invoices occurs in the background (as an asynchronous operation).</span></span>

### <a name="shared-service-vs-organization-based-exception-processing"></a><span data-ttu-id="3a8eb-197">Bendrai naudojama paslauga ir organizacija pagrįstas išimčių apdorojimas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-197">Shared service vs. organization-based exception processing</span></span>

<span data-ttu-id="3a8eb-198">Išimčių sąrašo puslapis palaiko standartines saugos struktūras, kurias **Duomenų valdymo** darbo sritis palaiko apdorojant išdėstymo įrašus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-198">The exceptions list page supports the standard security constructs that the **Data management** workspace supports for the processing of staging records.</span></span> <span data-ttu-id="3a8eb-199">SF importavimo užduotį galima apsaugoti šiais būdais:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-199">The invoice import job can be secured in the following ways:</span></span>

+ <span data-ttu-id="3a8eb-200">Pagal vartotojo vaidmenį</span><span class="sxs-lookup"><span data-stu-id="3a8eb-200">By user role</span></span>
+ <span data-ttu-id="3a8eb-201">Pagal vartotoją</span><span class="sxs-lookup"><span data-stu-id="3a8eb-201">By user</span></span>
+ <span data-ttu-id="3a8eb-202">Pagal juridinį subjektą</span><span class="sxs-lookup"><span data-stu-id="3a8eb-202">By legal entity</span></span>

![Importavimo užduotis, apsaugota pagal vartotojo vaidmenį ir juridinį subjektą](media/vendor_invoice_automation_04.png)

<span data-ttu-id="3a8eb-204">Jei sukonfigūruota SF importavimo užduoties sauga, išimčių sąrašo puslapis atsižvelgia į šiuos parametrus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-204">If security is configured for the invoice import job, the exceptions list page honors those settings.</span></span> <span data-ttu-id="3a8eb-205">Vartotojai galės matyti tik SF išimčių įrašus, kuriuos šis nustatymas leis jiems matyti.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-205">Users will be able to see only the invoice exception records that this setup allows them to see.</span></span>

<span data-ttu-id="3a8eb-206">Pvz., „Contoso“ nusprendė apdoroti SF išimtis pagal juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-206">For example, Contoso has decided to process invoice exceptions by legal entity.</span></span> <span data-ttu-id="3a8eb-207">Todėl SF importavimo užduoties sauga konfigūruojama taip, kad juridinio subjekto A vartotojas galėtų matyti tik SF išimtis juridiniame subjekte A, o juridinio subjekto B vartotojas galėtų matyti tik SF išimtis juridiniame subjekte B. Toks nustatymas leidžia atskirti SF išimčių tvarkymo pareigas.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-207">Therefore, security is configured on the invoice import job in such a way that a user in legal entity A can see only invoice exceptions in legal entity A, whereas a user in legal entity B can see only invoice exceptions in legal entity B. This setup enables segregation of duties for the management of invoice exceptions.</span></span>

<span data-ttu-id="3a8eb-208">Be to, „Contoso“ gali nuspręsti netaikyti jokios saugos, kad tie patys vartotojai galėtų apdoroti SF išimtis visuose juridiniuose subjektuose.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-208">Contoso could also decide not to enforce any security, so that the same users can process invoice exceptions for all legal entities.</span></span> <span data-ttu-id="3a8eb-209">Šis nustatymas įgalina SF išimčių tvarkymo bendrai naudojamų paslaugų scenarijų.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-209">This setup enables a shared services scenario for the management of invoice exceptions.</span></span>

## <a name="side-by-side-attachment-viewer"></a><span data-ttu-id="3a8eb-210">Priedų peržiūros vienas šalia kito žiūryklė</span><span class="sxs-lookup"><span data-stu-id="3a8eb-210">Side-by-side attachment viewer</span></span>

<span data-ttu-id="3a8eb-211">Kad galėtumėte lengvai peržiūrėti tiekėjo SF priedus, šiuose puslapiuose, kurie naudojami apdorojant SF, dabar pateikiama priedų žiūryklė:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-211">To help you easily view the attachments for vendor invoices, the following pages that are used in the invoicing process now provide an attachment viewer:</span></span>

+ <span data-ttu-id="3a8eb-212">**Išimčių tvarkymas**</span><span class="sxs-lookup"><span data-stu-id="3a8eb-212">**Exception handling**</span></span>
+ <span data-ttu-id="3a8eb-213">**Laukiančių tiekėjo SF** puslapis (taip pat pasiekiamas SF peržiūros procese)</span><span class="sxs-lookup"><span data-stu-id="3a8eb-213">**Pending vendor invoices** page (also available in the invoice review process)</span></span>
+ <span data-ttu-id="3a8eb-214">**SF žurnalo** užklausų puslapis (tik užregistruotoms SF)</span><span class="sxs-lookup"><span data-stu-id="3a8eb-214">**Invoice journal** inquiry page (for posted invoices)</span></span>

<span data-ttu-id="3a8eb-215">Čia pateiktos pagrindinės funkcijos, kurias suteikia priedų žiūryklė:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-215">Here is the main functionality that the attachment viewer provides:</span></span>

+ <span data-ttu-id="3a8eb-216">Peržiūrėkite visus priedų tipus, kuriuos palaiko dokumentų tvarkymas (failus, vaizdus, URL ir pastabas).</span><span class="sxs-lookup"><span data-stu-id="3a8eb-216">View all attachment types that Document management supports (files, images, URLs, and notes).</span></span>
+ <span data-ttu-id="3a8eb-217">Peržiūrėkite kelių puslapių TIFF failus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-217">View multi-page TIFF files.</span></span>
+ <span data-ttu-id="3a8eb-218">Su vaizdo failais atlikite nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-218">Perform the following actions on image files:</span></span>
  + <span data-ttu-id="3a8eb-219">Pažymėkite vaizdo dalis.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-219">Highlight parts of the image.</span></span>
  + <span data-ttu-id="3a8eb-220">Užblokuokite vaizdo dalis.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-220">Block parts of the image.</span></span>
  + <span data-ttu-id="3a8eb-221">Į vaizdą įtraukite komentarų.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-221">Add annotations to the image.</span></span>
  + <span data-ttu-id="3a8eb-222">Padidinkite ir sumažinkite vaizdo mastelį.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-222">Zoom in and out on the image.</span></span>
  + <span data-ttu-id="3a8eb-223">Nustatykite panoraminį vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-223">Pan the image.</span></span>
  + <span data-ttu-id="3a8eb-224">Anuliuokite ir perdarykite veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-224">Undo and redo actions.</span></span>
  + <span data-ttu-id="3a8eb-225">Pritaikykite vaizdo dydį.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-225">Fit the image to size.</span></span>

> [!NOTE]
> <span data-ttu-id="3a8eb-226">Šie veiksmai galimi tik vaizdo failams (JPEG, TIFF, PNG ir t. t.).</span><span class="sxs-lookup"><span data-stu-id="3a8eb-226">These actions are available only for image files (JPEG, TIFF, PNG, and so on).</span></span> <span data-ttu-id="3a8eb-227">Visi šiais veiksmais atlikti vaizdo pakeitimai įrašomi vaizdo faile.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-227">Any changes that you make to an image by using these actions are saved to the image file.</span></span> <span data-ttu-id="3a8eb-228">Šiuo metu priedų žiūryklė neapima versijų kūrimo arba audito galimybių.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-228">Currently, the attachment viewer doesn’t include versioning or auditing capabilities.</span></span>

### <a name="default-attachment"></a><span data-ttu-id="3a8eb-229">Numatytasis priedas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-229">Default attachment</span></span>

<span data-ttu-id="3a8eb-230">Jei tiekėjo SF yra daugiau nei vienas priedas, galite vieną iš dokumentų nustatyti kaip numatytąjį priedą puslapyje **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-230">If a vendor invoice has more than one attachment, you can set one of the documents as the default attachment on the **Attachments** page.</span></span> <span data-ttu-id="3a8eb-231">Parinktis **Numatytasis priedas** yra nauja į funkciją įtraukta parinktis.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-231">The **Is default attachment** option is a new option that was added as part of this feature.</span></span> <span data-ttu-id="3a8eb-232">Ši parinktis taip pat yra tiekėjo SF dokumentų priedų duomenų objekte.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-232">This option is also exposed in the Vendor invoice document attachment data entity.</span></span> <span data-ttu-id="3a8eb-233">Todėl numatytąjį priedą galima nustatyti integruojant.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-233">Therefore, the default attachment can be set through integrations.</span></span>

<span data-ttu-id="3a8eb-234">Tik vienas dokumentas gali būti nustatytas kaip numatytasis priedas.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-234">Only one document can be set as the default attachment.</span></span> <span data-ttu-id="3a8eb-235">Nustačius dokumentą kaip numatytąjį priedą jis automatiškai rodomas priedų žiūryklėje, kai atidaroma SF.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-235">After you set a document as the default attachment, it’s automatically shown in the attachment viewer when the invoice is opened.</span></span> <span data-ttu-id="3a8eb-236">Jeigu kaip numatytojo priedo nenustatote jokio dokumento, žiūryklė automatiškai nerodo jokio priedo, kai atidaroma SF.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-236">If you don’t set any document as the default attachment, the viewer doesn’t automatically show any attachment when the invoice is opened.</span></span>

### <a name="showhide-invoice-attachments"></a><span data-ttu-id="3a8eb-237">Rodyti / slėpti SF priedus</span><span class="sxs-lookup"><span data-stu-id="3a8eb-237">Show/hide invoice attachments</span></span>

<span data-ttu-id="3a8eb-238">Naujas mygtukas, pasiekiamas **Išimčių apdorojimo**, **Laukiančios SF** ir **SF žurnalo** užklausų puslapiuose, leidžia matyti arba paslepia priedų žiūryklę.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-238">A new button that is available on the **Exception processing**, **Pending invoice**, and **Invoice journal** inquiry pages lets you show or hide the attachment viewer.</span></span>

### <a name="security"></a><span data-ttu-id="3a8eb-239">Sauga</span><span class="sxs-lookup"><span data-stu-id="3a8eb-239">Security</span></span>

<span data-ttu-id="3a8eb-240">Nurodyti priedų žiūryklės veiksmai kontroliuojami naudojant vaidmenimis pagrįstą saugą:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-240">The following actions in the attachment viewer are controlled via role-based security:</span></span>

+ <span data-ttu-id="3a8eb-241">Žymėjimas</span><span class="sxs-lookup"><span data-stu-id="3a8eb-241">Highlighting</span></span>
+ <span data-ttu-id="3a8eb-242">Blokuoti</span><span class="sxs-lookup"><span data-stu-id="3a8eb-242">Block</span></span>
+ <span data-ttu-id="3a8eb-243">Komentaras</span><span class="sxs-lookup"><span data-stu-id="3a8eb-243">Annotation</span></span>

### <a name="pending-vendor-invoices-page"></a><span data-ttu-id="3a8eb-244">Laukiančių tiekėjo SF puslapis</span><span class="sxs-lookup"><span data-stu-id="3a8eb-244">Pending vendor invoices page</span></span>

<span data-ttu-id="3a8eb-245">Šios teisės suteikia tik skaitymo prieigą arba skaitymo / rašymo prieigą prie priedų žiūryklės, norint atlikti žymėjimo, blokavimo ir komentavimo veiksmus:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-245">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions:</span></span>

+ <span data-ttu-id="3a8eb-246">**Tvarkyti tiekėjo SF vaizdą** – ši teisė suteikia skaitymo / rašymo prieigą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-246">**Maintain vendor invoice image** – This privilege provides read/write access.</span></span>
+ <span data-ttu-id="3a8eb-247">**Peržiūrėti tiekėjo SF vaizdą** – ši teisė suteikia tik skaitymo prieigą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-247">**View vendor invoice image** – This privilege provides read-only access.</span></span>

<span data-ttu-id="3a8eb-248">Šios pareigos suteikia tik skaitymo arba skaitymo / rašymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-248">The following duties provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="3a8eb-249">**Tvarkyti tiekėjo SF** – šiai pareigai priskiriama teisė tvarkyti tiekėjo SF vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-249">**Maintain vendor invoices** – The Maintain vendor invoice image privilege is assigned to this duty.</span></span>
+ <span data-ttu-id="3a8eb-250">**Pateikti užklausą dėl tiekėjo SF būsenos** – šiai pareigai priskiriama teisė peržiūrėti tiekėjo SF vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-250">**Inquire into vendor invoice status** – The View vendor invoice image privilege is assigned to this duty.</span></span>

<span data-ttu-id="3a8eb-251">Šie vaidmenys suteikia tik skaitymo arba skaitymo / rašymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-251">The following roles provide read-only access or read/write access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="3a8eb-252">**Mokėtinų sumų klerkas** ir **Mokėtinų sumų vadovas** – tiekėjo SF tvarkymo pareiga priskiriama šiems vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-252">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>
+ <span data-ttu-id="3a8eb-253">**Mokėtinų sumų klerkas**, **Mokėtinų sumų vadovas**, **Mokėtinų sumų centralizuotų mokėjimų klerkas** ir **Mokėtinų sumų mokėjimų klerkas** – užklausų pateikimo dėl tiekėjo SF būsenos pareiga priskiriama šiems vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-253">**Accounts payable clerk**, **Accounts payable manager**, **Accounts payable centralized payments clerk**, and **Accounts payable payments clerk** – The Inquire into vendor invoice status duty is assigned to these roles.</span></span>

### <a name="invoice-exception-details-page"></a><span data-ttu-id="3a8eb-254">SF išimčių informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="3a8eb-254">Invoice exception details page</span></span>

<span data-ttu-id="3a8eb-255">Šios teisės suteikia tik skaitymo prieigą arba skaitymo / rašymo prieigą prie priedų žiūryklės, norint atlikti žymėjimo, blokavimo ir komentavimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-255">The following privileges provide ready-only access or read/write access to the attachment viewer for the highlighting, block, and annotation actions.</span></span>

> [!NOTE]
> <span data-ttu-id="3a8eb-256">Vaidmenys, kurie nurodyti šiame skyriuje, suteikia tik skaitymo prieigą prie SF vaizdų priedų žiūryklėje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-256">Out of the box, the roles that are mentioned in this section provide read-only access to the invoice images in the attachment viewer.</span></span> <span data-ttu-id="3a8eb-257">Jei vaidmeniui reikia ir rašymo prieigos prie vaizdų, galite suteikti rašymo prieigą tam vaidmeniui naudodami čia aprašytą teisę ir pareigą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-257">If a role must also have write access to the images, you can grant write access to that role by using the privilege and duty that are described here.</span></span>

+ <span data-ttu-id="3a8eb-258">**Tvarkyti tiekėjo SF antraštės objekto vaizdą** – ši teisė suteikia skaitymo / rašymo prieigą prie SF vaizdų priedų žiūryklėje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-258">**Maintain vendor invoice header entity image** – This privilege provides read/write access to the invoice images in the attachment viewer.</span></span>
+ <span data-ttu-id="3a8eb-259">**Peržiūrėti tiekėjo SF antraštės objekto vaizdą** – ši teisė suteikia tik SF vaizdo skaitymo rodinį priedų žiūryklėje.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-259">**View vendor invoice header entity image** – This privilege provides read-only view to the invoice image in the attachment viewer.</span></span>

<span data-ttu-id="3a8eb-260">Šios pareigos suteikia tik skaitymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-260">The following duties provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="3a8eb-261">**Tvarkyti tiekėjo SF** – šiai pareigai priskiriama teisė tvarkyti tiekėjo SF antraštės objekto vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-261">**Maintain vendor invoices** – The Maintain vendor invoice header entity image privilege is assigned to this duty.</span></span>

<span data-ttu-id="3a8eb-262">Šie vaidmenys suteikia tik skaitymo prieigą prie priedų žiūryklės norint atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="3a8eb-262">The following roles provide read-only access to the attachment viewer for those actions:</span></span>

+ <span data-ttu-id="3a8eb-263">**Mokėtinų sumų klerkas** ir **Mokėtinų sumų vadovas** – tiekėjo SF tvarkymo pareiga priskiriama šiems vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-263">**Accounts payable clerk** and **Accounts payable manager** – The Maintain vendor invoices duty is assigned to these roles.</span></span>

<span data-ttu-id="3a8eb-264">Pagal numatytuosius nustatymus, jei vartotojo vaidmuo suteikia bet kurio puslapio redagavimo teises, vartotojas taip pat turės redagavimo teises priedų žiūryklėje ir galės atlikti žymėjimo, blokavimo bei komentavimo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-264">By default, if the user role provides edit rights on any page, the user will also have edit rights on the attachments viewer for the highlighting, block, and annotation actions.</span></span> <span data-ttu-id="3a8eb-265">Tačiau jei yra scenarijų, kai tam tikras vaidmuo turi turėti redagavimo teises puslapyje, bet ne priedų žiūryklėje, tada galima naudoti tinkamas teises iš ankstesnio sąrašo.</span><span class="sxs-lookup"><span data-stu-id="3a8eb-265">However, if there are scenarios where a specific role should have edit rights on the page but not on the attachment viewer, the appropriate privileges from the preceding list can be used to satisfy the use case.</span></span>

