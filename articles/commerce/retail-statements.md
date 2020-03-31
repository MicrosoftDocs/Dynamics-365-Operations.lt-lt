---
title: Mažmeninės prekybos išrašai
description: Šioje temoje aprašoma, kaip kuriami ir registruojami išrašai.
author: ashishmsft
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 4409811d2ef60174a316db10307dc7af4697398c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023445"
---
# <a name="retail-statements"></a><span data-ttu-id="14a82-103">Mažmeninės prekybos išrašai</span><span class="sxs-lookup"><span data-stu-id="14a82-103">Retail statements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14a82-104">„Dynamics 365 Commerce“ išrašo registravimo procesas naudojamas kaip operacijos, vykdomos „Cloud point of sale“ (POS) arba „Modern POS“ (MPOS).</span><span class="sxs-lookup"><span data-stu-id="14a82-104">In Dynamics 365 Commerce, the statement posting process is used to account for the transactions that occur in Cloud point of sale (POS) or Modern POS (MPOS).</span></span> <span data-ttu-id="14a82-105">Išrašo registravimo procesas naudoja paskirstymo grafiką, kad EKA operacijų rinkinį perkeltų į būstinės (HQ) klientą.</span><span class="sxs-lookup"><span data-stu-id="14a82-105">The statement posting process uses the distribution schedule to pull a set of POS transactions into the headquarters (HQ) client.</span></span> <span data-ttu-id="14a82-106">Parametrai, kurie yra apibrėžti puslapiuose **„Commerce“ parametrai** ir **Parduotuvės**, yra naudojami operacijoms, kurios įtraukiamos į atskiras ataskaitas, pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="14a82-106">The parameters that are defined on the **Commerce parameters** and **Stores** pages are used to select the transactions that are pulled into individual statements.</span></span>

<span data-ttu-id="14a82-107">Išrašų registravimo procesas parodytas toliau pateiktame paveikslėlyje.</span><span class="sxs-lookup"><span data-stu-id="14a82-107">The following illustration shows the statement posting process.</span></span> <span data-ttu-id="14a82-108">Šiame procese EKA įrašytos operacijos perduodamos klientui naudojant „Commerce“ planavimo programą.</span><span class="sxs-lookup"><span data-stu-id="14a82-108">In this process, transactions that are recorded in the POS are transmitted to the client by using the Commerce scheduler.</span></span> <span data-ttu-id="14a82-109">Kai klientas gauna operacijas, galite kurti, skaičiuoti ir registruoti parduotuvės operacijos išrašą.</span><span class="sxs-lookup"><span data-stu-id="14a82-109">After the client receives the transactions, you can create, calculate, and post the transaction statement for the store.</span></span>

<span data-ttu-id="14a82-110">[![Išrašų registravimo procesas](./media/retail-statements.png)](./media/retail-statements.png)</span><span class="sxs-lookup"><span data-stu-id="14a82-110">[![Statement posting process](./media/retail-statements.png)](./media/retail-statements.png)</span></span>

## <a name="creating-and-posting-statements"></a><span data-ttu-id="14a82-111">Išrašų kūrimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="14a82-111">Creating and posting statements</span></span>

<span data-ttu-id="14a82-112">Galite kurti išrašą neautomatiniu būdu arba naudodami paketinius vykdymus, jūsų nustatytus reguliariai veikti visą dieną.</span><span class="sxs-lookup"><span data-stu-id="14a82-112">You can create a statement manually or by using batch processes that you set up to run periodically throughout the day.</span></span> <span data-ttu-id="14a82-113">Abiem atvejais išrašai kuriami ir registruojami atliekant toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="14a82-113">In both cases, the following steps are used to create and post statements.</span></span>

### <a name="create-the-statement"></a><span data-ttu-id="14a82-114">Išrašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="14a82-114">Create the statement</span></span>

<span data-ttu-id="14a82-115">Šiame veiksme identifikuojama parduotuvė, kuriai neautomatiniu būdu kuriamas išrašas.</span><span class="sxs-lookup"><span data-stu-id="14a82-115">This step identifies the store that the statement is manually created for.</span></span> <span data-ttu-id="14a82-116">Jei konfigūruojate paketinį vykdymą, galite automatiškai kurti išrašus visoms parduotuvėms pagal jūsų nustatytą grafiką.</span><span class="sxs-lookup"><span data-stu-id="14a82-116">If you configure a batch process, you can automatically create statements for all stores, based on a schedule that you define.</span></span>

### <a name="calculate-the-statement"></a><span data-ttu-id="14a82-117">Išrašo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="14a82-117">Calculate the statement</span></span>

<span data-ttu-id="14a82-118">Šiame etape operacijų eilutės parenkamos remiantis kriterijais, kurie kiekvienai parduotuvei yra nustatomi puslapiuose **„Commerce“ parametrai** ir **Parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="14a82-118">In this step, the transaction lines are selected based on criteria that are defined for each store on the **Commerce parameters** and **Stores** pages.</span></span> <span data-ttu-id="14a82-119">Šiuose puslapiuose galima apibrėžti kriterijus ir nurodyti, kaip skaičiuojamos operacijos.</span><span class="sxs-lookup"><span data-stu-id="14a82-119">On these pages, you define the criteria and specify how the transactions are calculated.</span></span> <span data-ttu-id="14a82-120">Jei norite peržiūrėti į išrašą įtrauktų operacijų sąrašą prieš skaičiuodami išrašą, naudokite puslapį **Operacijos**.</span><span class="sxs-lookup"><span data-stu-id="14a82-120">To view a list of the transactions that are included in the statement before you calculate the statement, use the **Transactions** page.</span></span>

<span data-ttu-id="14a82-121">Išrašo skaičiavime kaip apskaičiuota suma naudojamos mokėjimo priemonių deklaracijos iš registrų.</span><span class="sxs-lookup"><span data-stu-id="14a82-121">Statement calculation uses tender declarations from the registers as the counted amount.</span></span> <span data-ttu-id="14a82-122">Arba galite įvesti apskaičiuotą sumą neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="14a82-122">Alternatively, you can enter the counted amount manually.</span></span> <span data-ttu-id="14a82-123">Išraše nurodomas skirtumas tarp operacijų pardavimo sumos ir faktinės apskaičiuotos sumos visuose mokėjimo būduose.</span><span class="sxs-lookup"><span data-stu-id="14a82-123">The statement shows the difference between the sales amount for the transactions and the actual counted amount in all payment methods.</span></span> <span data-ttu-id="14a82-124">Išrašas registruojamas tik jei šis skirtumas yra mažesnis nei maksimalus registravimo skirtumas, nustatytas parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="14a82-124">The statement is posted only if this difference is less than the maximum posting difference that is defined for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="14a82-125">Išrašo skaičiavimo procese naudojama bendroji numeracija.</span><span class="sxs-lookup"><span data-stu-id="14a82-125">The statement calculation process uses the global number sequence.</span></span>

<span data-ttu-id="14a82-126">Kai skaičiuojate išrašą, skaičiavimas apima šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="14a82-126">When you calculate a statement, the calculation includes the following tasks:</span></span>

- <span data-ttu-id="14a82-127">Pažymėkite operacijas, kurios nebuvo įtrauktos į ankstesnio išrašo skaičiavimą, ir priskirkite pasirinktam datų intervalui.</span><span class="sxs-lookup"><span data-stu-id="14a82-127">For the selected date range, mark transactions that weren't included in a previous statement calculation.</span></span>
- <span data-ttu-id="14a82-128">Apskaičiuokite visas sumas, kurios buvo sumokėtos pasirinktose operacijose.</span><span class="sxs-lookup"><span data-stu-id="14a82-128">Calculate the total amounts that were tendered in the selected transactions.</span></span> <span data-ttu-id="14a82-129">Rezultatai rodomi išrašo eilutėse priklausomai nuo išrašo metodo.</span><span class="sxs-lookup"><span data-stu-id="14a82-129">The results are shown on the statement lines, depending on the statement method:</span></span>

    - <span data-ttu-id="14a82-130">Jei išrašo metodas yra **Iš viso**, eilutė sukuriama kiekvienam mokėjimo būdui pasirinktose operacijose.</span><span class="sxs-lookup"><span data-stu-id="14a82-130">If the statement method is **Total**, a line is created for each payment method in the selected transactions.</span></span>
    - <span data-ttu-id="14a82-131">Jei išrašo metodas yra **Personalas**, eilutė sukuriama kiekvienam mokėjimo būdui operacijose, kurias atliko pasirinktas personalo narys.</span><span class="sxs-lookup"><span data-stu-id="14a82-131">If the statement method is **Staff**, a line is created for each payment method in transactions that were performed by the selected staff member.</span></span>
    - <span data-ttu-id="14a82-132">Jei išrašo metodas yra **EKA terminalas**, eilutė sukuriama kiekvienam mokėjimo būdui operacijose, kurios buvo atliktos pasirinktame registre.</span><span class="sxs-lookup"><span data-stu-id="14a82-132">If the statement method is **POS terminal**, a line is created for each payment method in transactions that were performed on the selected register.</span></span>
    - <span data-ttu-id="14a82-133">Jei išrašo metodas yra **Pamaina**, eilutė sukuriama kiekvienam mokėjimo būdui operacijose, kurios buvo atliktos pamainos metu.</span><span class="sxs-lookup"><span data-stu-id="14a82-133">If the statement method is **Shift**, a line is created for each payment method in transactions that were performed during a shift.</span></span>

<span data-ttu-id="14a82-134">Jei puslapyje **Parduotuvės** pažymėtas žymės langelis **Skaidyti pagal išrašo metodą**, sukuriamas atskiras išrašas pagal reikšmę, pasirinktą lauke **Išrašo metodas**.</span><span class="sxs-lookup"><span data-stu-id="14a82-134">If the **Split by Statement method** check box is selected on the **Stores** page, a separate statement is created based on the value that is selected in the **Statement method** field.</span></span>

<span data-ttu-id="14a82-135">Jei jūsų parduotuvės darbo valandos tęsiasi ir po vidurnakčio, galite sukonfigūruoti išrašų registravimą pagal darbo dienos pabaigą, o ne pagal kalendorinės dienos pabaigą.</span><span class="sxs-lookup"><span data-stu-id="14a82-135">If your store's operating hours extend past midnight, you can configure statement posting so that it's based on the end of the business day instead of the end of the calendar day.</span></span>

<span data-ttu-id="14a82-136">Puslapio **Parduotuvės** „FastTab“ **Išrašas / uždarymas** lauke **Darbo dienos pabaiga** įveskite laiką, kada turi būti registruojama paskutinė operacija, kad ji būtų įtraukta į darbo dienos išrašą.</span><span class="sxs-lookup"><span data-stu-id="14a82-136">On the **Stores** page, on the **Statement/closing** FastTab, in the **End of business day** field, enter the time that the last transaction must be recorded to be included in the business day's statement.</span></span> <span data-ttu-id="14a82-137">Pažymėkite žymės langelį **Registruoti kaip darbo dieną**, jei norite registruoti operacijas tą pačią darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="14a82-137">Select the **Post as business day** check box to post the transactions within the same business day.</span></span> <span data-ttu-id="14a82-138">Užregistravus išrašą, operacijos, įrašytos tą pačią darbo dieną, gali būti įtrauktos į tą patį pardavimo užsakymą, net jei kai kurios operacijos vykdomos prieš vidurnaktį, o kitos operacijos – po vidurnakčio.</span><span class="sxs-lookup"><span data-stu-id="14a82-138">When the statement is posted, transactions that are recorded within the same business day can be included on the same sales order, even if some transactions occur before midnight and other transactions occur after midnight.</span></span>

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a><span data-ttu-id="14a82-139">Pavyzdys: darbo dienos, trunkančios dvi kalendorines dienas, išrašo registravimas</span><span class="sxs-lookup"><span data-stu-id="14a82-139">Example: Post a statement for a business day that extends over two calendar days</span></span>

<span data-ttu-id="14a82-140">Parduotuvė dirba nuo 8:00 val. iki 3:00 val., o parduotuvės konfigūracijoje pažymėtas žymės langelis **Registruoti kaip darbo dieną**.</span><span class="sxs-lookup"><span data-stu-id="14a82-140">A store is open between 8:00 AM and 3:00 AM, and the **Post as business day** check box is selected in the store's configuration.</span></span> <span data-ttu-id="14a82-141">Parduotuvė registruoja operacijas nuo gegužės 31 d. 8:00 val. iki vidurnakčio.</span><span class="sxs-lookup"><span data-stu-id="14a82-141">On May 31, the store records transactions between 8:00 AM and midnight.</span></span> <span data-ttu-id="14a82-142">Be to, parduotuvė registruoja operacijas nuo birželio 1 d. 12:01 val. iki 3:00 val.</span><span class="sxs-lookup"><span data-stu-id="14a82-142">The store also records transactions between 12:01 AM and 3:00 AM on June 1.</span></span>

<span data-ttu-id="14a82-143">Kai parduotuvė registruoja savo išrašą baigdama darbo dieną, generuojamas pardavimo užsakymas apima visas operacijas, įrašytas darbo valandomis nuo 8:00 val. iki 3:00 val., net jei operacijos įvyko dvi skirtingas dienas, gegužės 31 d. ir birželio 1 d.</span><span class="sxs-lookup"><span data-stu-id="14a82-143">When the store posts its statement for the close of the business day, the sales order that is generated includes all transactions that were recorded between the business hours of 8:00 AM and 3:00 AM, even though the transactions occurred on two days, May 31 and June 1.</span></span>

<span data-ttu-id="14a82-144">Jei ta pati parduotuvė konfigūruojama nepažymėjus žymės langelio **Registruoti kaip darbo dieną**, kai parduotuvė registruoja savo darbo dienos išrašą, generuojami atskiri pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="14a82-144">If the **Post as business day** check box is cleared for the same store, separate sales orders are generated when the store posts its statement for the close of the business day.</span></span> <span data-ttu-id="14a82-145">Vienas pardavimo užsakymas apima operacijas, įrašytas gegužės 31 d. darbo valandomis nuo 8:00 val. iki vidurnakčio, o antras – operacijas, įrašytas birželio 1 d. darbo valandomis nuo 12:01 val. iki 3:00 val.</span><span class="sxs-lookup"><span data-stu-id="14a82-145">One sales order includes the transactions that were recorded between the business hours of 8:00 AM and midnight on May 31, and the second sales order includes the transactions that were recorded between the business hours of 12:01 AM and 3:00 AM on June 1.</span></span>

> [!NOTE]
> <span data-ttu-id="14a82-146">Prieš kurdami išrašus turite uždaryti pamainas išrašo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="14a82-146">Before you can create statements, you should close the shifts in the statement period.</span></span>

### <a name="post-the-statement"></a><span data-ttu-id="14a82-147">Išrašo registravimas</span><span class="sxs-lookup"><span data-stu-id="14a82-147">Post the statement</span></span>

<span data-ttu-id="14a82-148">Kai skelbiate ataskaitą, pardavimo ataskaitoje sukuriami pardavimo užsakymai ir sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="14a82-148">When you post a statement, sales orders and invoices are created for the sales in the statement.</span></span>

- <span data-ttu-id="14a82-149">Atsiskaitymo grynaisiais operacijos kaupiamos viename pardavimo užsakyme, o sąskaita faktūra išrašoma numatytajam klientui, kuris yra priskirtas parduotuvei.</span><span class="sxs-lookup"><span data-stu-id="14a82-149">Cash and carry sales are aggregated onto one sales order, and are invoiced for the default customer who is assigned to the store.</span></span>
- <span data-ttu-id="14a82-150">Pardavimai, už kuriuos klientas buvo įtrauktas į operaciją, esančią EKA, sukuria atskirus pardavimo užsakymus ir SF, po vieną kiekvienam atskiram klientui.</span><span class="sxs-lookup"><span data-stu-id="14a82-150">Sales for which a customer was added to the transaction in POS generate separate sales orders and invoices, one for each unique customer.</span></span>

<span data-ttu-id="14a82-151">Išrašo mokėjimams automatiškai sukuriami mokėjimų žurnalai, o EKA parduotuvėje atnaujinamos atsargos.</span><span class="sxs-lookup"><span data-stu-id="14a82-151">Payment journals are automatically created for the payments in the statement, and the inventory is updated for the POS store.</span></span>