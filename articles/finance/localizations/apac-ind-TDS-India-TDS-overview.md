---
title: Indijos mokesčių, atskaitonų šaltinyje (TDS), peržiūra
description: Šioje temoje pateikiama išsami informacija apie Indijos mokestis, išskaičiuotas šaltinyje (TDS). TDS dokumentacijoje yra šios galimybės funkcijos.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023461"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="85632-104">Indijos mokesčių, atskaitonų šaltinyje (TDS), peržiūra</span><span class="sxs-lookup"><span data-stu-id="85632-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85632-105">Šioje temoje pateikiama išsami informacija apie Indijos mokestis, išskaičiuotas šaltinyje (TDS).</span><span class="sxs-lookup"><span data-stu-id="85632-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="85632-106">TDS dokumentacijoje yra šios galimybės funkcijos.</span><span class="sxs-lookup"><span data-stu-id="85632-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="85632-107">Taip pat paaiškinama, kaip atlikti pagrindinį TDS nustatymą, skaičiuoti TDS operacijas, užbaigti TDS sudengimo procesą, įrašyti TDS sertifikatų numerius ir generuoti TDS užklausas, TDS išrašus ir TDS sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="85632-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="85632-108">Dokumente yra šios temos:</span><span class="sxs-lookup"><span data-stu-id="85632-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="85632-109">Pagrindinis nustatymas TDS</span><span class="sxs-lookup"><span data-stu-id="85632-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="85632-110">Formulės konstruktoriaus ir ribinės ribos funkcija, naudojama TDS skaičiuoti</span><span class="sxs-lookup"><span data-stu-id="85632-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="85632-111">SF, mokėjimų, paprastųjų vekselių ir vidinės įmonės operacijų TDS skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="85632-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="85632-112">Periodinio TDS sudengimo procesas ir TDS sumų sudengimas TDS valdžios institucijos tiekėjams</span><span class="sxs-lookup"><span data-stu-id="85632-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="85632-113">TDS sertifikatų numerių ir datų įrašymas ir atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="85632-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="85632-114">Įvadas į TDS</span><span class="sxs-lookup"><span data-stu-id="85632-114">Introduction to TDS</span></span>

<span data-ttu-id="85632-115">Pagal 1961 m. Pajamų mokestį paslaugos gavėjas atskaičiuoja pajamų mokestį išankstinio mokėjimo arba kredito apskaitos metu, t. y. tas, kuris įvyksta anksčiau.</span><span class="sxs-lookup"><span data-stu-id="85632-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="85632-116">Asmuo, kuris atlieka mokėjimą, turi atskaityti mokesčio sumą ir sumokėti tik grynąjį balansą paslaugos teikėjui.</span><span class="sxs-lookup"><span data-stu-id="85632-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="85632-117">TDS taikomas paslaugoms, kurias nurodo vyriausybė, ir mokestis atskaitomas naudojant tarifus, kuriuos nurodo vyriausybė laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="85632-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="85632-118">Atskaitymo tarifas priklauso nuo objekto, kuris gauna mokėjimą arba teikia paslaugą, būsenos.</span><span class="sxs-lookup"><span data-stu-id="85632-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="85632-119">Būsenos apima **Atskirą**, **Hindu neatskirtą šeimą** (**HUF**), **Bendrovę**, **Firmą**, **Asmenų asociacijas** (**AOP**), **Asmenų subjektą** (**BOI**) ir **Vietos įstaigą**.</span><span class="sxs-lookup"><span data-stu-id="85632-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="85632-120">Šiose sekcijose pateikiamas paslaugų, kurios taikomos TDS, sąrašas, kaip nurodyta Indijos Vyriausybės.</span><span class="sxs-lookup"><span data-stu-id="85632-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="85632-121">**Gyventojų**</span><span class="sxs-lookup"><span data-stu-id="85632-121">**Residents**</span></span>

- <span data-ttu-id="85632-122">Pajamos iš atlyginimų (192 skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="85632-123">Pajamos iš palūkanų už vertybiniais popierius (193 skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="85632-124">Pajamos iš dividendų (194 skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="85632-125">Pajamos iš palūkanų (194A skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="85632-126">Pajamos iš loterių arba anfiltrų (194B skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="85632-127">Laimėjimai iš mėn. ir t. t. (Skyriuje 194BB)</span><span class="sxs-lookup"><span data-stu-id="85632-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="85632-128">Rangovai ir subrangovai (194C sekcijoje)</span><span class="sxs-lookup"><span data-stu-id="85632-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="85632-129">Draudimo komisiniai (194D skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="85632-130">Pajamos iš įmokų pagal šalies įrašymo schemą (194EE skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="85632-131">Pajamos iš socialinio fondo arba UI (194F skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="85632-132">Komisiniai, skirtuko, prizo ir pan., pardavimo ar kt. (194G skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="85632-133">Komisinių arba brokerio tarpininkavimo mokėjimas (pagal 194 H skyrių)</span><span class="sxs-lookup"><span data-stu-id="85632-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="85632-134">Nuoma (194I skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="85632-135">Profesinė paslauga (pagal 194J skyrių)</span><span class="sxs-lookup"><span data-stu-id="85632-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="85632-136">Pajamos iš vienetų (194K skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="85632-137">Tam tikros nuosavybės įsigijimo kompensacijos mokėjimas (194LA skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="85632-138">**Ne gyventojų**</span><span class="sxs-lookup"><span data-stu-id="85632-138">**Non-residents**</span></span>

- <span data-ttu-id="85632-139">Mokėjimai nenuo gyventojo sporto šakų asociacijai (194E skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="85632-140">Kitos sumos (195 skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="85632-141">Pajamos, atsižvelgiant į ne nuolatiniams vienetus (196A skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="85632-142">Pajamos iš Indijos įmonės užsienio valiutos obligacijų ar akcijų (196C skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="85632-143">Užsienio investuotojo pajamos iš apsaugos (196D skyriuje)</span><span class="sxs-lookup"><span data-stu-id="85632-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="85632-144">Atlyginimas ir visos kitos teigiamos pajamos iš bet kurio darbuotojo pajamoms (192 skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="85632-145">Vertybiniai popieriai (193 skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="85632-146">Palūkanos, kurios nėra palūkanos už vertybiniais popieriais (194A skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="85632-147">Mokėjimai rangovams ir subrangovams (194C skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="85632-148">Laimėjimai iš Yra arba kryžminių kodų (194B skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="85632-149">Laimėjimai iš žirgų lenktynių (194BB skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="85632-150">Draudimo komisiniai, padengiantys visus mokėjimus draudimo verslui įsigyti (194D skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="85632-151">Bet kokios palūkanos, kurios nėra palūkanos už vertybiniai popieriaii, mokėtini nenuodentiniams gyventojams, nėra įmonė ar užsienio įmonė (195 skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="85632-152">Mokėjimas nerezidentams sporto šakoms, įskaitant sporto asociacijas ar institucijas.</span><span class="sxs-lookup"><span data-stu-id="85632-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="85632-153">Jei nenuo gyventojas yra sporto šakininkas, reikia atlikti mokėjimus už skelbimus ir straipsnius bet kurioje Indijoje laikraščiuose, žurnaluose ir t. t.</span><span class="sxs-lookup"><span data-stu-id="85632-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="85632-154">įtrauktas į (194E skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="85632-155">Mokėjimas pagal NSS \[nacionalinių taupomųjų lėšų schemą\] (194EE skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="85632-156">Vienetų perpirkti pagal abipusius fondus arba UTI mokėjimas (194F skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="85632-157">Komisinių arba brokerio tarpininkavimo mokėjimas (pagal 194 H skyrių)</span><span class="sxs-lookup"><span data-stu-id="85632-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="85632-158">Nuomos mokėjimas (194I skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="85632-159">Mokesčių už profesines ar technines paslaugas mokėjimas (194J skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="85632-160">„Stockiest", platintojų, pirkėjų ir lėktuvų transporto transporto, įskaitant lėktuvo" (194G skyrius), komisiniai, įsakomasis ar prizas už šiuos bilietus</span><span class="sxs-lookup"><span data-stu-id="85632-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="85632-161">Pajamos iš vienetų, nupirktų užsienio valiuta, arba ilgalaikio kapitalo pelnas iš tokio vienetų, nupirktų užsienio valiuta, perkėlimo (196B skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="85632-162">Bet kokių pajamų mokėjimas ne nuolatiniams gyventojams palūkanų ar dividendų už obligacijas ir akcijas (196C skyrius)</span><span class="sxs-lookup"><span data-stu-id="85632-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="85632-163">TDS yra skaičiuojama pagal pirkimą, pardavimą, pardavimo grąžinimą, kredito pažymas, ilgalaikio turto įsigijimus, išankstinius apmokėjimus, išankstinius mokėjimus, paprastus vekselius, darbų mokesčius ir vidinės įmonės operacijas.</span><span class="sxs-lookup"><span data-stu-id="85632-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="85632-164">Dabartiniame Indijos mokesčių scenarijuje TDS nėra skaičiuojamas pagal pardavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="85632-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="85632-165">Tačiau sistema apima atidėjimus, pagal kurias apskaičiuojamas pardavimo, ypač vidinės įmonės operacijų, susigrąžinamas TDS.</span><span class="sxs-lookup"><span data-stu-id="85632-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="85632-166">Skaičiuojant TDS visada atsižvelgiama į ribinę vertę ir išimties ribinę vertę, kuri nustatyta TDS komponentui.</span><span class="sxs-lookup"><span data-stu-id="85632-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="85632-167">Turi būti paleistas periodinis TDS sudengimo procesas ir TDS mokėjimai turi būti sudengti TDS institucijų tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="85632-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="85632-168">Iš tiekėjų ar klientų gautų TDS sertifikatų numerius ir datas galima įrašyti ir atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="85632-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="85632-169">Be to, 26Q formas ir 27Q ketvirčio išrašus bei TDS 16A sertifikatą galima generuoti finansuose.</span><span class="sxs-lookup"><span data-stu-id="85632-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="85632-170">Nustatymas ir darbas su TDS</span><span class="sxs-lookup"><span data-stu-id="85632-170">Setting up and working with TDS</span></span>

<span data-ttu-id="85632-171">Toliau pateikiama nustatymo ir darbo su TDS proceso apžvalga:</span><span class="sxs-lookup"><span data-stu-id="85632-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="85632-172">**TDS nustatyumai:**</span><span class="sxs-lookup"><span data-stu-id="85632-172">**TDS setup:**</span></span>

    - <span data-ttu-id="85632-173">Parametrų nustatymas:</span><span class="sxs-lookup"><span data-stu-id="85632-173">Parameter setup:</span></span>

        - <span data-ttu-id="85632-174">DK parametruose suaktyvinkite su TDS susijusius parametrus.</span><span class="sxs-lookup"><span data-stu-id="85632-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="85632-175">DK parametruose nustatykite išskaitomų mokesčių mokėjimų numeraciją.</span><span class="sxs-lookup"><span data-stu-id="85632-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="85632-176">Parametrų mokėtinos sąskaitose ir gautinose sąskaitose nustatymas.</span><span class="sxs-lookup"><span data-stu-id="85632-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="85632-177">Pagrindinė sąranka:</span><span class="sxs-lookup"><span data-stu-id="85632-177">Basic setup:</span></span>

        - <span data-ttu-id="85632-178">Nustatykite įmonės, klientų ir tiekėjų TDS registracijos numerius.</span><span class="sxs-lookup"><span data-stu-id="85632-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="85632-179">Nustatyti TDS elemento grupes.</span><span class="sxs-lookup"><span data-stu-id="85632-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="85632-180">Nustatykite TDS komponentus, pridėkite TDS komponentų grupes ir nustatykite jų ribinę vertę ir išimties ribą.</span><span class="sxs-lookup"><span data-stu-id="85632-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="85632-181">Nustatyti TDS institucijas.</span><span class="sxs-lookup"><span data-stu-id="85632-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="85632-182">TDS sudengimo laikotarpių nustatymas.</span><span class="sxs-lookup"><span data-stu-id="85632-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="85632-183">Nustatykite TDS mokesčių kodus ir pridėkite prie jų TDS komponentus.</span><span class="sxs-lookup"><span data-stu-id="85632-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="85632-184">Nustatykite TDS grupes ir pridėkite prie jų TDS mokesčių kodus.</span><span class="sxs-lookup"><span data-stu-id="85632-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="85632-185">Formulės konstruktoriuje nurodykite formulę, pagal kurią skaičiuojamas TDS grupės TDS.</span><span class="sxs-lookup"><span data-stu-id="85632-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="85632-186">Įrašykite TDS koncesijos sertifikato numerius.</span><span class="sxs-lookup"><span data-stu-id="85632-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="85632-187">DK sąskaitos ir įmonės nustatymas:</span><span class="sxs-lookup"><span data-stu-id="85632-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="85632-188">Nustatykite TDS mokėtinas ir gautinas DK sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="85632-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="85632-189">Nustatykite įmonės mokesčių atskaitymo ir rinkinio sąskaitos numerį (TAN) ir atskaitymo tipo kategoriją.</span><span class="sxs-lookup"><span data-stu-id="85632-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="85632-190">Kitas nustatymas:</span><span class="sxs-lookup"><span data-stu-id="85632-190">Other setup:</span></span>

        - <span data-ttu-id="85632-191">Nustatyti mokėjimo grafiką, kuriame yra TDS paskirstymas.</span><span class="sxs-lookup"><span data-stu-id="85632-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="85632-192">Nustatykite mokėjimo mokesčių tipą mokėjimams TDS institucijai.</span><span class="sxs-lookup"><span data-stu-id="85632-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="85632-193">Nustatyti informaciją apie TDS grupes, nuolatinius sąskaitų numerius (PAN) ir TN tiekėjams ir klientams.</span><span class="sxs-lookup"><span data-stu-id="85632-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="85632-194">**TDS skaičiavimas operacijose:**</span><span class="sxs-lookup"><span data-stu-id="85632-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="85632-195">SF ir mokėjimai</span><span class="sxs-lookup"><span data-stu-id="85632-195">Invoices and payments</span></span>
    - <span data-ttu-id="85632-196">Paprastieji vekseliai</span><span class="sxs-lookup"><span data-stu-id="85632-196">Promissory notes</span></span>
    - <span data-ttu-id="85632-197">Išankstinis mokėjimas</span><span class="sxs-lookup"><span data-stu-id="85632-197">Advance payments</span></span>
    - <span data-ttu-id="85632-198">Išankstiniai mokėjimai</span><span class="sxs-lookup"><span data-stu-id="85632-198">Prepayments</span></span>

3. <span data-ttu-id="85632-199">**TDS atsiskaitymas**</span><span class="sxs-lookup"><span data-stu-id="85632-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="85632-200">Periodinio TDS sudengimo procesas</span><span class="sxs-lookup"><span data-stu-id="85632-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="85632-201">TDS mokėjimų TDS valdžios tiekėjams sudengimas ir TDS išdavimo generavimas</span><span class="sxs-lookup"><span data-stu-id="85632-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="85632-202">**TDS užklausos, išrašai ir sertifikatas:**</span><span class="sxs-lookup"><span data-stu-id="85632-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="85632-203">TDS sertifikato numerių ir datų įrašas ir naujinimas.</span><span class="sxs-lookup"><span data-stu-id="85632-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="85632-204">Generuoti TDS užklausą ir užregistruotą TDS užklausą.</span><span class="sxs-lookup"><span data-stu-id="85632-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="85632-205">Generuoti 27A formą, 26Q formą ir 27Q TDS formą ir ketvirčio el.TDS išrašus.</span><span class="sxs-lookup"><span data-stu-id="85632-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="85632-206">Kurti 16A TDS sertifikato formą.</span><span class="sxs-lookup"><span data-stu-id="85632-206">Generate a Form 16A TDS certificate.</span></span>
