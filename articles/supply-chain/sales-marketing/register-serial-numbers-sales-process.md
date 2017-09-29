---
title: "Serijinių numerių registravimas pardavimo procese"
description: "Šiame straipsnyje paaiškinama, kaip pardavimo proceso metu galite registruoti važtaraščių ar SF serijos numerius. Ši funkcija naudinga, jei įmonė nori užfiksuoti serijos numerius paslaugų ir garantijos tikslais, tačiau nenori tvarkyti serijos numerių atsargose nuo gavimo iki išdavimo."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResTrackingDimensionGroup, InventTrackingRegisterTrans, SalesEditLines, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 28931
ms.assetid: 5d39630f-607e-492b-8c1e-790ca53effa0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 55cb0f20dbd671e39d0f409a87cec93efd9ce4d6
ms.openlocfilehash: 9b8f66d4b62b43b3a62af8d39631e7cd7f688a11
ms.contentlocale: lt-lt
ms.lasthandoff: 07/07/2017


---

# <a name="register-serial-numbers-in-the-sales-process"></a><span data-ttu-id="f4728-104">Serijinių numerių registravimas pardavimo procese</span><span class="sxs-lookup"><span data-stu-id="f4728-104">Register serial numbers in the sales process</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

<span data-ttu-id="f4728-105">Šiame straipsnyje paaiškinama, kaip pardavimo proceso metu galite registruoti važtaraščių ar SF serijos numerius.</span><span class="sxs-lookup"><span data-stu-id="f4728-105">This articles explains how you can register serial numbers on packing slips or invoices during the sales process.</span></span> <span data-ttu-id="f4728-106">Ši funkcija naudinga, jei įmonė nori užfiksuoti serijos numerius paslaugų ir garantijos tikslais, tačiau nenori tvarkyti serijos numerių atsargose nuo gavimo iki išdavimo.</span><span class="sxs-lookup"><span data-stu-id="f4728-106">This functionality is useful if a company wants to capture serial numbers for service and warranty purposes, but doesn't have to maintain serial numbers in inventory from receipt to issue.</span></span>

<span data-ttu-id="f4728-107">Daug įmonių tiesiog nori užfiksuoti serijinius numerius paslaugų ir garantijos tikslais, ir nenori turėti serijinių numerių atsargose nuo gavimo iki išdavimo.</span><span class="sxs-lookup"><span data-stu-id="f4728-107">Many companies just want to capture serial numbers for service and warranty purposes, and don't have to maintain serial numbers in inventory from receipt to issue.</span></span> <span data-ttu-id="f4728-108">Šiose situacijose „Microsoft Dynamics 365 for Finance and Operations“ važtaraščių ar sąskaitų faktūrų serijos numerius leidžia registruoti produktus parduodant.</span><span class="sxs-lookup"><span data-stu-id="f4728-108">In these scenarios, Microsoft Dynamics 365 for Finance and Operations lets you register the serial numbers on the packing slips or invoices when products are sold.</span></span> <span data-ttu-id="f4728-109">Jei produktai yra vėliau grąžinami, galite atsekti kiekvieną produktą sąskaitoje faktūroje ir nustatyti, ar pardavėte produktą ar paslaugą ir ar galioja garantiniai įsipareigojimai.</span><span class="sxs-lookup"><span data-stu-id="f4728-109">If products are later returned, you can trace each product to an invoice to determine whether you sold the product, and whether the service or warranty obligations are valid.</span></span>
<span data-ttu-id="f4728-110">Ar yra kokių nors būtinųjų sąlygų?</span><span class="sxs-lookup"><span data-stu-id="f4728-110">Are there any prerequisites?</span></span>
----------------------------

<span data-ttu-id="f4728-111">Pardavimo procesui turite įjungti serijinius numerius, pasirinkdami **Aktyvus pardavimų procese** parinktį iš **Sekimo dimensijos grupių** puslapio.</span><span class="sxs-lookup"><span data-stu-id="f4728-111">You must enable serial numbers for the sales process by selecting the **Active in sales process** option on the **Tracking dimension groups** page.</span></span> <span data-ttu-id="f4728-112">Tada sprendime „Microsoft Dynamics 365 for Finance and Operations“ įvyksta tolesni įvykiai.</span><span class="sxs-lookup"><span data-stu-id="f4728-112">The following events then occur in Microsoft Dynamics 365 for Finance and Operations:</span></span>
-   <span data-ttu-id="f4728-113">Iš **Serijos numerių** „FastTab“ pasirenkama **Serijos numerių kontrolė** parinktis.</span><span class="sxs-lookup"><span data-stu-id="f4728-113">On the **Serial numbers** FastTab, the **Serial number control** option is selected.</span></span> <span data-ttu-id="f4728-114">Pažymėję šią parinktį, turite užregistruoti vieną serijinį numerį kiekvienai prekei ant važtaraščio arba sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="f4728-114">When this option is selected, you must register one serial number for each item on the packing slip or invoice.</span></span>
-   <span data-ttu-id="f4728-115">Visi serijinių numerių pasirinkimai sekimo dimensijų grupėje anuliuojami, išskyrus **Galimas tuščias išdavimas** parinktį.</span><span class="sxs-lookup"><span data-stu-id="f4728-115">All selections on the tracking dimension group for serial numbers are cleared, except the **Blank issue allowed** option.</span></span> <span data-ttu-id="f4728-116">Galite pasirinkti **Galimas tuščias išdavimas** parinktį, norėdami nepaisyti serijos numerių kontrolės, ir leisti supakuoti prekes ir išrašyti sąskaitą neužregistravę serijos numerių.</span><span class="sxs-lookup"><span data-stu-id="f4728-116">You can select the **Blank issue allowed** option to override the serial number control, and allow products to be packed and invoiced without registering serial numbers.</span></span>

## <a name="when-do-i-register-serial-numbers-during-the-sales-process"></a><span data-ttu-id="f4728-117">Kada užregistruoti serijos numerius pardavimo proceso metu?</span><span class="sxs-lookup"><span data-stu-id="f4728-117">When do I register serial numbers during the sales process?</span></span>
<span data-ttu-id="f4728-118">Serijos numerius galite užregistruoti ant pardavimo užsakymo važtaraščio arba sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="f4728-118">You can register serial numbers either on the packing slip for a sales order or on the invoice.</span></span> <span data-ttu-id="f4728-119">Kai paruošite sąskaitą faktūrą serijos prekei, kuri atgabenta kartu su važtaraščiu, galite pasirinkti, kurie serijos numeriai ant važtaraščio bus įtraukti į sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="f4728-119">When you prepare an invoice for a serialized item that was shipped together with a packing slip, you can select which serial numbers on the packing slip to invoice.</span></span> <span data-ttu-id="f4728-120">Registruotų serijos numerių skaičius neturi viršyti atgabentų prekių kiekio.</span><span class="sxs-lookup"><span data-stu-id="f4728-120">The number of registered serial numbers must not exceed the quantity of items that were shipped.</span></span> <span data-ttu-id="f4728-121">Jei kuriate dalinę sąskaitą faktūrą, galite pasirinkti mažiau serijos prekių nei įregistruota važtaraštyje.</span><span class="sxs-lookup"><span data-stu-id="f4728-121">If you're creating a partial invoice, you can select fewer serialized items than were registered on the packing slip.</span></span> <span data-ttu-id="f4728-122">Kai spausdinate važtaraštį arba sąskaitą faktūrą, įtraukiami serijos numeriai, kurie buvo užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="f4728-122">When you print a packing slip or an invoice, the serial numbers that were registered are included.</span></span>

## <a name="can-i-enter-serial-numbers-by-scanning-them-or-do-i-have-to-type-them"></a><span data-ttu-id="f4728-123">Ar galiu įvesti serijos numerius juos nuskaitant, ar juos reikia spausdinti?</span><span class="sxs-lookup"><span data-stu-id="f4728-123">Can I enter serial numbers by scanning them, or do I have to type them?</span></span>
<span data-ttu-id="f4728-124">Galite nuskaityti arba spausdinti serijos numerius.</span><span class="sxs-lookup"><span data-stu-id="f4728-124">You can either scan or type serial numbers.</span></span> <span data-ttu-id="f4728-125">Kai naudojate skaitytuvą, skenavimas režimas nustato, ar serijos numeriai yra įvedami, ar pašalinami iš serijos numerių sąskaitoje faktūroje arba važtaraščio sąrašo.</span><span class="sxs-lookup"><span data-stu-id="f4728-125">When you use a scanner, the scan mode determines whether the serial numbers are added to or removed from the list of serial numbers on the invoice or packing slip.</span></span> <span data-ttu-id="f4728-126">Jei norite nuskaityti serijos numerius, naudodami, pavyzdžiui, rankinį brūkšninių kodų skaitytuvą, sukonfigūruokite skaitytuvą siuntimui, paspaudę Enter arba TAB komandą po serijos numerio.</span><span class="sxs-lookup"><span data-stu-id="f4728-126">If you want to scan serial numbers  by using, for example, a hand-held bar code scanner, configure the scanner to send an Enter or TAB command after the serial number.</span></span> <span data-ttu-id="f4728-127">Ši komanda nurodo duomenų srauto pabaigą.</span><span class="sxs-lookup"><span data-stu-id="f4728-127">This command will indicate the end of the data stream.</span></span> <span data-ttu-id="f4728-128">Priešingu atveju, nuskaitę kiekvieną serijos numerį turite spausti Enter arba TAB ant klaviatūros.</span><span class="sxs-lookup"><span data-stu-id="f4728-128">Otherwise, you must press Enter or TAB on the keyboard after you scan each serial number.</span></span>

## <a name="if-i-enable-serial-numbers-for-the-sales-process-do-i-have-to-register-all-serial-numbers-for-all-items"></a><span data-ttu-id="f4728-129">Jei įjungsiu serijos numerius pardavimo procesui, ar turėsiu registruoti visus serijos numerius visoms prekėms?</span><span class="sxs-lookup"><span data-stu-id="f4728-129">If I enable serial numbers for the sales process, do I have to register all serial numbers for all items?</span></span>
<span data-ttu-id="f4728-130">Prekei priskirtos sekimo dimensijos grupės sąranka nustato, ar serijos numerius reikia registruoti visoms prekėms sąskaitoje faktūroje arba važtaraštyje.</span><span class="sxs-lookup"><span data-stu-id="f4728-130">The setup of the tracking dimension group that is assigned to the product determines whether serial numbers must be registered for all items on a packing slip or invoice.</span></span> <span data-ttu-id="f4728-131">Įjungus serijos numerius pardavimo procesui, automatiškai pasirenkama **Serijos numerių kontrolės** parinktis.</span><span class="sxs-lookup"><span data-stu-id="f4728-131">When you enable serial numbers for the sales process, the **Serial number control** option is automatically selected.</span></span> <span data-ttu-id="f4728-132">Tada turite užregistruoti vieną serijos numerį arba užregistruoti tuščią registraciją už neįskaitomam skaičiui kiekvienos prekės apie važtaraštyje arba sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="f4728-132">You must then register one serial number, or register a blank registration for an unreadable number, for each item on the packing slip or invoice.</span></span> <span data-ttu-id="f4728-133">Jei nenorite reikalauti serijos numerio kiekvienai prekei, pasirinkite **Galimi tušti išdavimai** parinktį sekimo dimensijos grupėje, kuri priskirta prekei.</span><span class="sxs-lookup"><span data-stu-id="f4728-133">If you don't want to require a serial number for each item, select the **Blank issue allowed** option on the tracking dimension group that is assigned to the item.</span></span> <span data-ttu-id="f4728-134">Tada galite registruoti mažiau serijos numerių, nei gabenamų prekių kiekis.</span><span class="sxs-lookup"><span data-stu-id="f4728-134">You can then register fewer serial numbers than the quantity of items that are being shipped.</span></span> <span data-ttu-id="f4728-135">Jei užregistruosite daugiau serijos numerių, nei gabenamų prekių kiekis, negalėsite išrašyti važtaraštį arba sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="f4728-135">If you register more serial numbers than the quantity of items that are being shipped, you won't be able to post the packing slip or invoice.</span></span>

## <a name="can-i-register-serial-numbers-for-partial-invoices-and-partial-shipments"></a><span data-ttu-id="f4728-136">Ar galiu registruoti serijos numerius dalinėms sąskaitoms faktūroms ir dalinėms siuntoms?</span><span class="sxs-lookup"><span data-stu-id="f4728-136">Can I register serial numbers for partial invoices and partial shipments?</span></span>
<span data-ttu-id="f4728-137">Galite kurti dalines sąskaitas faktūras ir važtaraščius pardavimų užsakymams ir registruoti tik serijos numerius tų prekių, kurios yra įtrauktos į sąskaitas faktūras ir važtaraščius.</span><span class="sxs-lookup"><span data-stu-id="f4728-137">You can create partial invoices and packing slips for sales orders, and register only the serial numbers for the items that those invoices and packing slips include.</span></span> <span data-ttu-id="f4728-138">Jei norite sukurti dalinę sąskaitą faktūrą ir turite daugiau nei vieną važtaraštį vienam pardavimo užsakymui, galite įtraukti serijos numerius iš daugiau nei vieno važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="f4728-138">If you want to create a partial invoice, and you have more than one packing slip for the sales order, you can include serial numbers from more than one packing slip.</span></span> <span data-ttu-id="f4728-139">Tačiau gali būti tik vienas važtaraštis, neapimantis visų serijos numerių.</span><span class="sxs-lookup"><span data-stu-id="f4728-139">However, there can be only one packing slip that doesn't include all serial numbers.</span></span> <span data-ttu-id="f4728-140">Pavyzdžiui, jei turite tris važtaraščius, ir kiekvienas važtaraštis apima dvi serijos prekes, negalite sukurti dalinės sąskaitos faktūros vienai prekei iš kiekvieno važtaraščio.</span><span class="sxs-lookup"><span data-stu-id="f4728-140">For example, if you have three packing slips, and each packing slip includes two serialized items, you can't create a partial invoice for one item from each packing slip.</span></span>

## <a name="what-do-i-do-when-a-serial-number-isnt-readable"></a><span data-ttu-id="f4728-141">Ką daryti, kai serijos numeris yra neįskaitomas?</span><span class="sxs-lookup"><span data-stu-id="f4728-141">What do I do when a serial number isn't readable?</span></span>
<span data-ttu-id="f4728-142">Jei serijos numeris neįskaitomas ir nenuskanuojamas, galite sukurti prekei tuščią eilutę, paspaudę **Neįskaitomas** **Serijos numerių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f4728-142">If a serial number can't be read or scanned, you can create a blank line for the item by clicking **Not readable** on the **Serial numbers** page.</span></span> <span data-ttu-id="f4728-143">Jei serijos numeris tampa žinomas vėliau, galite atnaujinti sąskaitą faktūrą ar važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="f4728-143">If the serial number becomes available later, you can update the invoice or packing slip.</span></span> <span data-ttu-id="f4728-144">Norėdami gauti daugiau informacijos, skaitykite kitą skyrių „Ar galiu pataisyti arba pakeisti serijos numerius užregistruotam pardavimo užsakymui?“</span><span class="sxs-lookup"><span data-stu-id="f4728-144">For more information, see the next section, “Can I correct or change the serial numbers I have registered for a sales order?”</span></span>

## <a name="can-i-correct-or-change-the-serial-numbers-that-i-have-registered-for-a-sales-order"></a><span data-ttu-id="f4728-145">Ar galiu pataisyti arba pakeisti serijos numerius užregistruotam pardavimo užsakymui?</span><span class="sxs-lookup"><span data-stu-id="f4728-145">Can I correct or change the serial numbers that I have registered for a sales order?</span></span>
<span data-ttu-id="f4728-146">Taip, galite ištaisyti serijos numerius, jei įvykdomos šios sąlygos:</span><span class="sxs-lookup"><span data-stu-id="f4728-146">Yes, you can correct serial numbers if the following conditions are met:</span></span>
-   <span data-ttu-id="f4728-147">**Sąskaitos** – galite pakeisti serijos numerius prekių, kurioms dar neišrašėte sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="f4728-147">**Invoices** – You can change the serial numbers for items that you haven't yet invoiced.</span></span> <span data-ttu-id="f4728-148">Tada atnaujinamas ir važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="f4728-148">The packing slip is then also updated.</span></span> <span data-ttu-id="f4728-149">Tačiau jei pardavimo užsakymo eilutė buvo ištaisyta registruojant neigiamą kiekį, serijos numerių pardavimo užsakymo eilutei pakeisti negalite.</span><span class="sxs-lookup"><span data-stu-id="f4728-149">However, if a sales order line was corrected by registering a negative quantity, you can't change serial numbers for the sales order line.</span></span>
-   <span data-ttu-id="f4728-150">**Važtaraščiai** – galite dalinai pataisyti važtaraščio eilutę, kurioje yra serijos prekės.</span><span class="sxs-lookup"><span data-stu-id="f4728-150">**Packing slips** – You can't partially correct a packing slip line that contains serialized items.</span></span> <span data-ttu-id="f4728-151">Turite atšaukti visą tos eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="f4728-151">You must reverse the full quantity for the line.</span></span> <span data-ttu-id="f4728-152">Jeigu važtaraštis buvo atšauktas arba taisytas, nereikia vėl registruoti atvirkštinių serijos numerių, kai kuriate naują tų pačių serijinių prekių važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="f4728-152">If a packing slip has been canceled or corrected, you don't have to register the reversed serial numbers again when you create a new packing slip for the same serialized items.</span></span> <span data-ttu-id="f4728-153">Bus naudojami užregistruoti numeriai.</span><span class="sxs-lookup"><span data-stu-id="f4728-153">The numbers that were registered will be used.</span></span>

## <a name="can-i-view-the-serial-numbers-that-were-shipped-together-with-a-specific-packing-slip-or-that-were-included-on-an-invoice"></a><span data-ttu-id="f4728-154">Ar galiu peržiūrėti serijos numerius, atsiųstus kartu su konkrečiu važtaraščiu, arba tuos, kurie buvo įtraukti į sąskaitą faktūrą?</span><span class="sxs-lookup"><span data-stu-id="f4728-154">Can I view the serial numbers that were shipped together with a specific packing slip, or that were included on an invoice?</span></span>
<span data-ttu-id="f4728-155">Taip, galite atlikti užklausą važtaraščio žurnalo eilutėje arba sąskaitos faktūros žurnalo eilutėje ir peržiūrėti visų serijos numerių, įtrauktų į tą dokumentą, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f4728-155">Yes, you can run an inquiry on the packing slip journal line or invoice journal line to view a list of all serial numbers that were included in the document.</span></span>

## <a name="can-i-view-the-serialized-items-that-i-have-on-hand"></a><span data-ttu-id="f4728-156">Ar galiu peržiūrėti savo turimas prekes su serijos numeriais?</span><span class="sxs-lookup"><span data-stu-id="f4728-156">Can I view the serialized items that I have on hand?</span></span>
<span data-ttu-id="f4728-157">Ne, negalite peržiūrėti serijos prekių, kurias turite po ranka, nes serijiniai numeriai neregistruojami tol, kol prekės neparduodamos.</span><span class="sxs-lookup"><span data-stu-id="f4728-157">No, you can't view the serialized items that you have on hand, because serial numbers aren't registered for items until the items are sold.</span></span>

## <a name="can-i-register-serial-numbers-for-catchweight-items"></a><span data-ttu-id="f4728-158">Ar galiu registruoti esamo svorio prekių serijos numerius?</span><span class="sxs-lookup"><span data-stu-id="f4728-158">Can I register serial numbers for catchweight items?</span></span>
<span data-ttu-id="f4728-159">Ne, negalite registruotis serijos numerių sveriamoms prekėms pardavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="f4728-159">No, you can't register serial numbers for catch-weight items during the sales process.</span></span> <span data-ttu-id="f4728-160">Be to, jei prekė nustatyta kaip sveriama, negalite priskirti prekės sekimo dimensijos grupei, kuri skirta naudoti serijos numerius tik pardavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="f4728-160">Additionally, if a product is set up as a catch-weight item, you can't assign the product to a tracking dimension group that is set up to use serial numbers only during the sales process.</span></span>
<span data-ttu-id="f4728-161">Ar galiu registruoti serijos numerius mažmeninės prekybos EKA?</span><span class="sxs-lookup"><span data-stu-id="f4728-161">Can I register serial numbers at the retail POS?</span></span>
------------------------------------------------

<span data-ttu-id="f4728-162">Taip, mažmeninės prekybos taškas (EKA) paskatins vartotoją įvesti serijos numerį, kai vartotojas parduoda prekę, kuri yra priskirta sekimo dimensijos grupei, kuri yra sukurta naudoti serijos numerius tik pardavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="f4728-162">Yes, the retail point of sale (POS) will prompt the user to enter a serial number when the user sells an item that is assigned a tracking dimension group that is set up to use serial numbers only during the sales process.</span></span>

## <a name="what-security-roles-are-required-in-order-to-register-serial-numbers-during-the-sales-process"></a><span data-ttu-id="f4728-163">Kokie saugos vaidmenys yra privalomi norint įregistruoti serijos numerius pardavimo proceso metu??</span><span class="sxs-lookup"><span data-stu-id="f4728-163">What security roles are required in order to register serial numbers during the sales process?</span></span>
<span data-ttu-id="f4728-164">Ši funkcija yra prieinama visiems vaidmenims, kurie gali tvarkyti pardavimų važtaraščius ir pardavimo sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="f4728-164">This functionality is available to all roles that can maintain sales packing slips and sales invoices.</span></span> <span data-ttu-id="f4728-165">Šie vaidmenys leidžia darbuotojams redaguoti serijos numerius ir registruoti tuščius serijos numerių įrašus, kurių negalima įskaityti ar nuskenuoti:</span><span class="sxs-lookup"><span data-stu-id="f4728-165">The following duties let workers correct serial numbers, and register blank entries for serial numbers that can't be read or scanned:</span></span>
-   <span data-ttu-id="f4728-166">Tvarkyti serijos numerių koregavimą</span><span class="sxs-lookup"><span data-stu-id="f4728-166">Maintain serial number corrections</span></span>
-   <span data-ttu-id="f4728-167">Tvarkyti neįskaitomų serijos numerių registravimą</span><span class="sxs-lookup"><span data-stu-id="f4728-167">Maintain registration of non-readable serial numbers</span></span>





