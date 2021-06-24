---
title: Pastabų integravimas
description: Šioje temoje aprašomas pastabų duomenų integravimas dvigubo rašymo funkcijoje.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: ceb5b7c90cc7efa0049d0278e2c245228e5b52bd
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186791"
---
# <a name="note-integration"></a><span data-ttu-id="b3cd9-103">Pastabų integravimas</span><span class="sxs-lookup"><span data-stu-id="b3cd9-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b3cd9-104">Verslo procesų metu „Microsoft Dynamics 365” vartotojai dažnai renka informaciją apie savo klientus.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="b3cd9-105">Ši informacija įrašoma kaip veiklos ir pastabos.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="b3cd9-106">Šioje temoje aprašomas pastabų duomenų integravimas dvigubo rašymo funkcijoje.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="b3cd9-107">Kliento informaciją galima klasifikuoti toliau pateiktais būdais.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="b3cd9-108">**Veiksminga informacija, kurią „Dynamics 365“ vartotojas valdo kliento vardu** – Pavyzdžiui, „Contoso“ („Dynamics 365“ vartotojas) veda žaidimų šou.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="b3cd9-109">Vienas Iš „Contoso“ klientų (klientas) nori dalyvauti žaidimų šou.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="b3cd9-110">Klientas paprašo „Contoso“ darbuotojo rezervuoti jam vietą žaidimų šou.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="b3cd9-111">Rezervavimas įvyksta „Contoso“ įvykių dalyvio kalendoriuje.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="b3cd9-112">**Veiksminga „Dynamics 365” vartotojo informacija** – pvz., klientas, perkantis „Surface” vienetą, įveda specialias instrukcijas, nurodančias, kad prieš pristatant įrenginį reikia supakuoti kaip dovaną.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="b3cd9-113">Šios instrukcijos yra veiksmingos informacijos, kurią turi valdyti „Contoso“ darbuotojas, atsakingas už pakavimą.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="b3cd9-114">**Neveiksminga informacija** – pvz., klientas lankosi „Contoso“ parduotuvėje ir pokalbio su parduotuvės atstovu metu išreiškia susidomėjimą *„Halo“* žaidimais bei žaidimų priedais.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="b3cd9-115">Parduotuvės atstovas pasižymi šios informacijos pastabą.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="b3cd9-116">Tada produktų rekomendacijų mechanizmas ją naudoja, kad klientui pateiktų rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="b3cd9-117">Apskritai, veiksminga informacija fiksuojama kaip *veiklos* „Finance and Operations” bei klientų įtraukimo programose.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="b3cd9-118">Neveiksminga informacija fiksuojama kaip *pastabos* „Finance and Operations” programose arba kaip *komentarai* klientų įtraukimo programose.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="b3cd9-119">Nors pastabos skirtos neveiksmingai informacijai, programos netrukdys jomis naudotis saugant ir valdant veiksmingą informaciją, jei norite jas naudoti tokiu būdu.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="b3cd9-120">„Microsoft” šiuo metu leidžia pastabų integravimo funkcijas.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="b3cd9-121">(Veiklos integravimo funkcijos bus išleistos vėliau.) Pastabų integravimą galima naudoti dirbant su klientais, tiekėjais, pardavimo užsakymais ir pirkimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="b3cd9-122">Pastabos kūrimas klientų įtraukimo programoje</span><span class="sxs-lookup"><span data-stu-id="b3cd9-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="b3cd9-123">Norėdami sukurti pastabą klientų įtraukimo programoje ir tada sinchronizuoti ją su „Finance and Operations” programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b3cd9-124">Klientų įtraukimo programoje atidarykite kliento abonemento įrašą.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="b3cd9-125">Srityje **Laiko juosta** pasirinkite pliuso ženklą (**+**), tada, norėdami sukurti pastabą, pasirinkite **Pastaba**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Pastabos kūrimas klientų įtraukimo programoje](media/notes-ce-1.png)

3. <span data-ttu-id="b3cd9-127">Įveskite pavadinimą ir aprašymą, tada pasirinkite **Įtraukti pastabą**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-127">Enter a title and description, and then select **Add note**.</span></span>

    ![Pavadinimo ir aprašymo įvedimas](media/notes-ce-2.png)

    <span data-ttu-id="b3cd9-129">Nauja pastaba įtraukiama į kliento laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-129">The new note is added to the customer timeline.</span></span>

    ![Nauja pastaba kliento laiko juostoje](media/notes-ce-3.png)

4. <span data-ttu-id="b3cd9-131">Prisijunkite prie „Finance and Operations” programos ir atidarykite tą patį kliento įrašą.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="b3cd9-132">Atkreipkite dėmesį, kad viršutiniame dešiniajame kampe esantis mygtukas **Priedai** (sąvaržėlės simbolis) nurodo, kad įrašas turi priedą.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![Pranešimas apie priedą](media/notes-ce-4.png)

5. <span data-ttu-id="b3cd9-134">Pasirinkite mygtuką **Priedai**, kad atidarytumėte puslapį **Priedai**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="b3cd9-135">Turėtumėte rasti pastabą, kurią sukūrėte klientų įtraukimo programoje.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Pastaba iš klientų įtraukimo programos](media/notes-ce-5.png)

<span data-ttu-id="b3cd9-137">Visi pastabos atnaujinimai sinchronizuojami tarp „Finance and Operations” programos ir klientų įtraukimo programos.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="b3cd9-138">Pastabos kūrimas „Finance and Operations” programoje</span><span class="sxs-lookup"><span data-stu-id="b3cd9-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="b3cd9-139">Taip pat galite sukurti pastabą „Finance and Operations” programoje ir ji bus sinchronizuojama su klientų įtraukimo programa.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="b3cd9-140">Norėdami sukurti pastabą „Finance and Operations” programoje ir tada sinchronizuoti ją su klientų įtraukimo programa, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="b3cd9-141">Programos „Finance and Operations” puslapyje **Priedai** pasirinkite **Naujas** \> **Pastaba**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Pastabos kūrimas „Finance and Operations” programoje](media/notes-fo-1.png)

2. <span data-ttu-id="b3cd9-143">Įveskite pavadinimą ir trumpą instrukcijų rinkinį, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![Pavadinimo ir instrukcijų įvedimas](media/notes-fo-2.png)

3. <span data-ttu-id="b3cd9-145">Atnaujinkite įrašą klientų įtraukimo programoje.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="b3cd9-146">Naują pastabą turėtumėte rasti laiko juostoje.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-146">You should find the new note on the timeline.</span></span>

    ![Nauja pastaba klientų įtraukimo programos laiko juostoje](media/notes-fo-3.png)

<span data-ttu-id="b3cd9-148">Pastabą galite klasifikuoti kaip vidinę arba išorinę.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="b3cd9-149">Programos „Finance and Operations” puslapyje **Priedai** atidarykite pastabą, tada lauke **Apribojimas** pasirinkite **Vidinis** arba **Išorinis**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Laukas Apribojimas](media/notes-fo-4.png)

<span data-ttu-id="b3cd9-151">Taip pat galite sukurti URL.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-151">You can also create a URL.</span></span>

1. <span data-ttu-id="b3cd9-152">Programos „Finance and Operations” puslapyje **Priedai** pasirinkite **Naujas** \> **URL**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="b3cd9-153">Įveskite pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="b3cd9-154">Lauke **Apribojimas** pasirinkite **Vidinis** arba **Išorinis**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![URL kūrimas „Finance and Operations” programoje](media/notes-fo-5.png)

4. <span data-ttu-id="b3cd9-156">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-156">Select **Save**.</span></span>

    <span data-ttu-id="b3cd9-157">Kadangi klientų įtraukimo programų URL tipo nėra, URL integruotas su dvigubu rašymu kaip pastaba.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![URL kaip pastaba klientų įtraukimo programoje](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="b3cd9-159">Failų priedai nepalaikomi.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="b3cd9-160">Šablonai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-160">Templates</span></span>

<span data-ttu-id="b3cd9-161">Pastabų integravimą sudaro lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="b3cd9-162">„Finance and Operations“ programa</span><span class="sxs-lookup"><span data-stu-id="b3cd9-162">Finance and Operations app</span></span> | <span data-ttu-id="b3cd9-163">„Customer engagement“ programa</span><span class="sxs-lookup"><span data-stu-id="b3cd9-163">Customer engagement app</span></span> | <span data-ttu-id="b3cd9-164">aprašymas</span><span class="sxs-lookup"><span data-stu-id="b3cd9-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="b3cd9-165">Kliento priedai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="b3cd9-166">Komentarai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-166">Annotations</span></span> | <span data-ttu-id="b3cd9-167">Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių klientų informaciją (organizacijų ir asmenų).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="b3cd9-168">Tiekėjo dokumentų priedai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="b3cd9-169">Komentarai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-169">Annotations</span></span> | <span data-ttu-id="b3cd9-170">Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių tiekėjų informaciją (organizacijų ir asmenų).</span><span class="sxs-lookup"><span data-stu-id="b3cd9-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="b3cd9-171">Pardavimo užsakymo antraštės dokumento priedai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="b3cd9-172">Komentarai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-172">Annotations</span></span> | <span data-ttu-id="b3cd9-173">Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių pardavimo užsakymų informaciją.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="b3cd9-174">Pirkimo užsakymo antraštės dokumento priedai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="b3cd9-175">Komentarai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-175">Annotations</span></span> | <span data-ttu-id="b3cd9-176">Įmonės, naudojančios paprastąjį tekstą ir URL, kad fiksuotų konkrečių pirkimo užsakymų informaciją.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

## <a name="limitations"></a><span data-ttu-id="b3cd9-177">Apribojimai</span><span class="sxs-lookup"><span data-stu-id="b3cd9-177">Limitations</span></span>

<span data-ttu-id="b3cd9-178">Įdiegę pastabų sprendimą, jo pašalinti negalite.</span><span class="sxs-lookup"><span data-stu-id="b3cd9-178">Once you install the notes solution, you cannot uninstall it.</span></span> 

<span data-ttu-id="b3cd9-179">Daugiau informacijos žr. [Dvigubo rašymo susiejimo nuoroda](mapping-reference.md)</span><span class="sxs-lookup"><span data-stu-id="b3cd9-179">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>
