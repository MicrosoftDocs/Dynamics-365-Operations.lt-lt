---
title: Grąžinimų valdymo modulio apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Supply Chain Management” grąžinimo valdymo modulio apžvalga.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 826cee7b1e30020aec99f6148dd9ab16f126c417
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839130"
---
# <a name="rebate-management-module-overview"></a><span data-ttu-id="3ffe5-103">Grąžinimų valdymo modulio apžvalga</span><span class="sxs-lookup"><span data-stu-id="3ffe5-103">Rebate management module overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3ffe5-104">Galite naudoti **Grąžinimų valdymo** modulį kurti kontraktams, sandoriams ar sutartims tarp jūsų verslo ir jo klientų arba tiekėjų, kad būtų galima apskaičiuoti grąžinimus, atskaitymus ir autorinius honorarus.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-104">You can use the **Rebate management** module to create contracts, deals, or agreements between your business and its customers or vendors, so that you can calculate rebates, deductions, and royalties.</span></span> <span data-ttu-id="3ffe5-105">Grąžinimo valdymas seka ir prižiūri grąžinimo ir atskaitymo operacijas centrinėje vietoje, kurioje vartotojai gali jas efektyviai kurti, peržiūrėti ir apdoroti.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-105">Rebate management tracks and maintains rebate and deduction transactions in a central location where users can effectively create, review, and process them.</span></span>

<span data-ttu-id="3ffe5-106">Grąžinimų valdymas palaiko *grąžinimų* kūrimą, priežiūrą ir apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-106">Rebate management supports the creation, maintenance, and processing of *rebates*.</span></span> <span data-ttu-id="3ffe5-107">Grąžinimas yra pirkimo kainos dalies grąžinimas pirkėjui arba pardavėjui.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-107">A rebate is the return of part of the purchase price by a seller or a buyer.</span></span> <span data-ttu-id="3ffe5-108">Grąžinimai paprastai yra grindžiami konkretaus kiekio arba vertės prekių pirkimu tam tikru laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-108">Rebates are typically based on the purchase of a specific quantity or value of goods during a specific period.</span></span> <span data-ttu-id="3ffe5-109">Skirtingai nei nuolaidos, grąžinimai atliekami po to, kai pirkimo sumai pilnai išrašoma sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-109">Unlike discounts, rebates are done after the purchase amount is fully invoiced.</span></span>

<span data-ttu-id="3ffe5-110">Grąžinimų valdymas taip pat palaiko *atskaitymus*.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-110">Rebate management also supports *deductions*.</span></span> <span data-ttu-id="3ffe5-111">Atskaitymas yra kompensacija, atlyginimas arba mokestis, mokamas už licenciją arba mokestį, siekiant naudoti intelektinę nuosavybę, pavyzdžiui, prekės ženklą, autoriaus teisės arba patentą, taip pat už teisę naudoti gamtos išteklius žvejybos, medžioklės ar kasybos tikslais.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-111">A deduction is compensation, a consideration, or a fee that is paid either for a license or the privilege to use intellectual property such as a brand, copyright, or patent, or for the privilege to use a natural resource for a purpose such as for fishing, hunting, or mining.</span></span> <span data-ttu-id="3ffe5-112">Atskaitymai paprastai apskaičiuojami kaip procentas nuo įplaukų arba pelno nuo realizuoto panaudojimo.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-112">Deductions are usually calculated as a percentage of the revenue or profit from realized use.</span></span> <span data-ttu-id="3ffe5-113">Kuo daugiau naudojama intelektinė nuosavybė arba gamtos ištekliai, tuo didesnis atskaitymas.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-113">The more the intellectual property or natural resource is used, the greater the deduction that is realized.</span></span>

<span data-ttu-id="3ffe5-114">Taip pat, grąžinimo valdymas palaiko kliento *autorinius honorarus*.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-114">Additionally, Rebate management supports customer *royalties*.</span></span> <span data-ttu-id="3ffe5-115">Autoriniai honorarai yra mokėjimai, kuriuos viena šalis atlieka licencijos savininkui arba franšizei už teisę naudotis turtu.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-115">Royalties are payments that one party makes to the licensee or franchisee for the right to use an asset.</span></span>

<span data-ttu-id="3ffe5-116">Grąžinimų valdymas leidžia jums apibrėžti nuostatų, grąžinimų ir nurašymų registravimo šablonus.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-116">Rebate management lets you define posting profiles for provisions, rebates, and write-offs.</span></span> <span data-ttu-id="3ffe5-117">Be to, galima nurodyti konkretaus kliento arba tiekėjo registravimus.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-117">Furthermore, the postings can be defined for a specific customer or vendor.</span></span> <span data-ttu-id="3ffe5-118">Tokiu būdu, pasiūlymai, kurie netaikomi visiems klientų ar tiekėjų scenarijams, gali būti sekami naudojant registravimus.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-118">In this way, deals that don't apply to all customer or vendor scenarios can be tracked via postings.</span></span>

<span data-ttu-id="3ffe5-119">Grąžinimo operacijos generuojamos automatiškai, remiantis paketinėms užduotims pasirinktu ir suplanuotu skaičiavimo metodu.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-119">Rebate transactions are automatically generated, based on the calculation method that is selected and scheduled in batch jobs.</span></span> <span data-ttu-id="3ffe5-120">Taip pat, galite nustatyti darbo eigas sutartims valdyti, peržiūrėti ir tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-120">Additionally, you can set up workflows to manage, review, and approve agreements.</span></span>

## <a name="basis-calculation"></a><span data-ttu-id="3ffe5-121">Pagrindas skaičiavimui</span><span class="sxs-lookup"><span data-stu-id="3ffe5-121">Basis calculation</span></span>

<span data-ttu-id="3ffe5-122">Kliento grąžinimai, kliento autoriniai honorarai ir tiekėjo grąžinimai gali naudoti skirtingą pagrindą, atsižvelgiant į jūsų verslo reikalavimus:</span><span class="sxs-lookup"><span data-stu-id="3ffe5-122">Customer rebates, customer royalties, and vendor rebates can all use a different basis, depending on your business requirements:</span></span>

- <span data-ttu-id="3ffe5-123">Kliento grąžinimai gali būti pagrįsti pardavimo užsakymais, pristatymo pastabomis arba sąskaitomis faktūromis.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-123">Customer rebates can be based on sales orders, delivery notes, or invoices.</span></span>
- <span data-ttu-id="3ffe5-124">Kliento autoriniai honorarai gali būti pagrįsti pardavimo užsakymais, pristatymo pastabomis arba apmokėtomis sąskaitomis faktūromis.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-124">Customer royalties can be based on sales orders, delivery notes, or paid invoices.</span></span>
- <span data-ttu-id="3ffe5-125">Tiekėjo grąžinimai gali būti pagrįsti pirkimo arba pardavimo užsakymais.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-125">Vendor rebates can be based on either purchase orders or sales orders.</span></span> <span data-ttu-id="3ffe5-126">Jie gali būti apskaičiuojami pagal produktus, kurie yra perkami iš grąžinimo tiekėjo ir parduodami klientams pagal pardavimo sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-126">They can be calculated based on products that are purchased from the rebate vendor and sold to customers via sales invoices.</span></span>

## <a name="flexible-calculations"></a><span data-ttu-id="3ffe5-127">Lankstūs skaičiavimai</span><span class="sxs-lookup"><span data-stu-id="3ffe5-127">Flexible calculations</span></span>

<span data-ttu-id="3ffe5-128">Grąžinimo skaičiavimo laikotarpius galima naudoti tiek klientų, tiek tiekėjų sandorių atvejais.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-128">Rebate calculation periods are available for both customer deals and vendor deals.</span></span> <span data-ttu-id="3ffe5-129">Skaičiavimo laikotarpis nurodo sandorio ilgį, skaičiavimo dažnį ir laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-129">A calculation period defines the length of the deal, the calculation frequency, and the calculation period.</span></span> <span data-ttu-id="3ffe5-130">Grąžinimai gali būti sukaupti remiantis pardavimo užsakymo kiekiais arba patvirtintų produktų sumomis grąžinimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-130">The rebates can be accrued based on the sales order quantities or amounts for qualified products during the rebate period.</span></span>

<span data-ttu-id="3ffe5-131">Kiekvienam sutarties skaičiavimui galima nustatyti bet kurį iš šių laikotarpių:</span><span class="sxs-lookup"><span data-stu-id="3ffe5-131">For each agreement calculation, any of the following periods can be set:</span></span>

- <span data-ttu-id="3ffe5-132">Sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="3ffe5-132">Invoice</span></span>
- <span data-ttu-id="3ffe5-133">Diena</span><span class="sxs-lookup"><span data-stu-id="3ffe5-133">Day</span></span>
- <span data-ttu-id="3ffe5-134">Savaitė</span><span class="sxs-lookup"><span data-stu-id="3ffe5-134">Week</span></span>
- <span data-ttu-id="3ffe5-135">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="3ffe5-135">Month</span></span>
- <span data-ttu-id="3ffe5-136">Ketvirtis</span><span class="sxs-lookup"><span data-stu-id="3ffe5-136">Quarter</span></span>
- <span data-ttu-id="3ffe5-137">Metai</span><span class="sxs-lookup"><span data-stu-id="3ffe5-137">Year</span></span>
- <span data-ttu-id="3ffe5-138">Pritaikytas laikotarpis</span><span class="sxs-lookup"><span data-stu-id="3ffe5-138">Customized period</span></span>
- <span data-ttu-id="3ffe5-139">Bet kuris kartotinis iš anksčiau išvardintų laikotarpių</span><span class="sxs-lookup"><span data-stu-id="3ffe5-139">Any multiple of any of the previously listed periods</span></span>

<span data-ttu-id="3ffe5-140">Skaičiavimas gali būti taikomas atskiriems klientams ir produktams, klientų ir produktų grupėms arba visiems klientams ir produktams.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-140">The calculation can be applied to individual customers and products, groups of customers and products, or all customers and products.</span></span> <span data-ttu-id="3ffe5-141">Grąžinimai, turintis kelias išsamios informacijos eilutes, gali turėti skirtingus tinkamumo datos diapazonus.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-141">Rebates that have multiple detail lines can have different qualifying date ranges.</span></span> <span data-ttu-id="3ffe5-142">Nuostatos ir pareikalavimo laikotarpiai gali skirtis.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-142">The provision and claim periods can differ.</span></span> <span data-ttu-id="3ffe5-143">Pavyzdžiui, nuostatos gali būti apdorojamos kiekvieną dieną, o pareikalavimai – kartą per mėnesį.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-143">For example, provisions can be processed every day, whereas claims are processed once per month.</span></span>

<span data-ttu-id="3ffe5-144">Grąžinimus galima konfigūruoti pagal daug skirtingų parametrų.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-144">Rebates can be configured based on many different parameters.</span></span> <span data-ttu-id="3ffe5-145">Pavyzdžiui, juos galima konfigūruoti kaip procentą, tarifą arba fiksuotą sumą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-145">For example, they can be configured as a percentage, a rate, or a fixed amount.</span></span> <span data-ttu-id="3ffe5-146">Yra keturi pagrindiniai skaičiavimo metodai:</span><span class="sxs-lookup"><span data-stu-id="3ffe5-146">There are four main calculation methods:</span></span>

- <span data-ttu-id="3ffe5-147">Žingsninis</span><span class="sxs-lookup"><span data-stu-id="3ffe5-147">Stepped</span></span>
- <span data-ttu-id="3ffe5-148">Sukauptas</span><span class="sxs-lookup"><span data-stu-id="3ffe5-148">Cumulative</span></span>
- <span data-ttu-id="3ffe5-149">Sumavimas</span><span class="sxs-lookup"><span data-stu-id="3ffe5-149">Rolling</span></span>
- <span data-ttu-id="3ffe5-150">Bendroji vertė</span><span class="sxs-lookup"><span data-stu-id="3ffe5-150">Total value</span></span>

<span data-ttu-id="3ffe5-151">Grąžinimo skaičiavimo rezultatai taip pat gali būti sumažinti kitais grąžinimais, atsižvelgiant į tai, ar grąžinimas nustatytas skaičiuoti pagal grynąją sumą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-151">Rebate calculation results can also be reduced by other rebates, depending on whether the rebate is set up to calculate based on the net amount.</span></span>

<span data-ttu-id="3ffe5-152">Iš tiekėjo pusės grąžinimai gali apskaičiuoti kainą pagal pirmas ateina, pirmas išeina (FIFO) taisyklę, naujausio pirkimo kainą, vidutinę pirkimo kainą arba pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-152">On the vendor side, rebates can calculate the price based on a first in, first out (FIFO) rule, the latest purchase price, the average purchase price, or the sales price.</span></span>

## <a name="rebate-target-transactions"></a><span data-ttu-id="3ffe5-153">Grąžinimų paskirties operacijos</span><span class="sxs-lookup"><span data-stu-id="3ffe5-153">Rebate target transactions</span></span>

<span data-ttu-id="3ffe5-154">Išvestis, kurias sugeneruoja grąžinimų sandoris arba sutartis, gali būti finansai arba prekės.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-154">The outputs that the rebate deal or agreement generates can be financials or items.</span></span>

<span data-ttu-id="3ffe5-155">Finansinės išvestis nustatomos pagal mokėjimo tipą, priskirtą sutarčiai iš registravimo šablono.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-155">Financial outputs are determined by the payment type that is assigned to the agreement from the posting profile.</span></span> <span data-ttu-id="3ffe5-156">Šias išvestis gali sudaryti kliento atskaitymų žurnalai, laisvos formos ir tiekėjų sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-156">These outputs can include customer deduction journals, free text invoices, and vendor invoices.</span></span> <span data-ttu-id="3ffe5-157">Audito tikslais finansinės grąžinimų paskirties operacijos apima nuorodą į pirminę grąžinimo sutartį.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-157">For auditing purposes, financial rebate target transactions include a reference to the originating rebate agreement.</span></span>

<span data-ttu-id="3ffe5-158">Prekių išvestys sukuria laisvos prekės pardavimo užsakymą, skirtą kliento grąžinimams, ir pirkimo užsakymą, skirtą tiekėjų grąžinimams.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-158">Item outputs create a free item sales order for customer rebates and a purchase order for vendor rebates.</span></span> <span data-ttu-id="3ffe5-159">Prekės grąžinimų paskirties operacijose yra parinkčių, nustatančių, kuri grąžinimo nuoroda turi būti įvesta į laisvos prekės pardavimo arba pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-159">Item rebate target transactions contain options to determine which rebate reference should be entered on the free item sales order or purchase order.</span></span>

## <a name="accurate-rebate-calculations"></a><span data-ttu-id="3ffe5-160">Tikslūs grąžinimų skaičiavimai</span><span class="sxs-lookup"><span data-stu-id="3ffe5-160">Accurate rebate calculations</span></span>

<span data-ttu-id="3ffe5-161">Pasirinktų susietų sandorių, skaičiavimų dažnumo, skaičiavimo pagrindo ir skaičiavimo metodo derinys lemia grąžinimo skaičiavimų tikslumą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-161">The combination of the associated deals, the frequency of the calculations, the calculation basis, and the calculation method that is selected determines the accuracy and precision of rebate calculations.</span></span> <span data-ttu-id="3ffe5-162">Grąžinimų nuostatos gali būti naudojamos užregistruotų ir pareikalautų verčių kaupimui.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-162">Rebate provisions can be used to accrue posted and claimed values.</span></span>

<span data-ttu-id="3ffe5-163">Nuostatas galima tvarkyti kas dieną arba kas mėnesį.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-163">Provisions can be managed daily or monthly.</span></span> <span data-ttu-id="3ffe5-164">Tačiau funkcija gali paskirstyti arba apmokėti grąžinimą, taip pat gauti jo apmokėjimą bet kokiu apibrėžtu dažnumu.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-164">However, the functionality can allocate or pay the rebate, or receive payment of it, at any defined frequency.</span></span> <span data-ttu-id="3ffe5-165">Vartotojai gali bet kuriuo apmokėjimo metu nesunkiai koreguoti planą ar mokėjimo sumas.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-165">Users can easily adjust a plan or payment amounts at any time during the payout.</span></span>

<span data-ttu-id="3ffe5-166">Vartotojams nebereikia tvarkyti sandorių ar nuostatų dvejais veiksmais.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-166">Users no longer have to handle deals or provisions in two steps.</span></span> <span data-ttu-id="3ffe5-167">Nuostatos ir nurašymai yra registruojami tiesiogiai į didžiąją knygą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-167">Provisions and write-offs are posted directly to the ledger.</span></span> <span data-ttu-id="3ffe5-168">Taip pat, kredito pažymas galima kurti automatiškai.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-168">Additionally, credit notes can be created automatically.</span></span> <span data-ttu-id="3ffe5-169">Taigi, mokėtinos ir gautinos sumos yra visiškai suintegruotos.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-169">Therefore, there is full integration with accounts payable and accounts receivable.</span></span> <span data-ttu-id="3ffe5-170">Atliekant skaičiavimus atsižvelgiama į sudengimo nuolaidas, apmokėtas sąskaitas faktūras, prekybos nuolaidas ir esamas kredito pažymas, siekiant užtikrinti, kad sumos ir vertės yra tiksliai apskaičiuojamos.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-170">During processing, the calculations consider settlement discounts, paid invoices, trade discounts, and existing credit notes to ensure that amounts and values are accurately calculated.</span></span>

<span data-ttu-id="3ffe5-171">Apskaičiavus grąžinimus, procesas sukuria operacijas, kurias galima peržiūrėti prieš registravimą.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-171">When rebates are calculated, the process creates transactions that can be reviewed before posting occurs.</span></span> <span data-ttu-id="3ffe5-172">Tada galima sukurti žurnalą, kredito pažymą arba debeto operaciją.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-172">A journal, credit note, or debit transaction can then be created.</span></span> <span data-ttu-id="3ffe5-173">Atskiru procesu registruojamos grąžinimų ir atskaitymų operacijos.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-173">A separate process posts rebate and deduction transactions.</span></span> <span data-ttu-id="3ffe5-174">Norint užtikrinti atitikimą, efektyvumą ir skaidrumą, galima gauti ataskaitų išrašus ir operacijų sąrašus.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-174">Reporting statements and transaction listings can be obtained to ensure compliance, effectiveness, and transparency.</span></span>

## <a name="guaranteed-royalty-payments"></a><span data-ttu-id="3ffe5-175">Garantiniai autorinių honorarų mokėjimai</span><span class="sxs-lookup"><span data-stu-id="3ffe5-175">Guaranteed royalty payments</span></span>

<span data-ttu-id="3ffe5-176">Naudojant grąžinimų valdymą, automatinis mokėjimų generavimas leidžia greitai ir lengvai tvarkyti autorinius honorarus, net jei taikomi garantiniai minimumai.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-176">In Rebate management, automatic payment generation enables royalties to be handled quickly and easily, even when guaranteed minimums apply.</span></span> 

## <a name="maximizing-spend-versus-rebates"></a><span data-ttu-id="3ffe5-177">Maksimalių išlaidos ir grąžinimai</span><span class="sxs-lookup"><span data-stu-id="3ffe5-177">Maximizing spend versus rebates</span></span>

<span data-ttu-id="3ffe5-178">Tiekėjai ir produktai gali būti sugrupuoti pagal teritoriją, o skirtingi pasiūlymai gali būti pateikti, atsižvelgiant į operacijos šalį arba regioną.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-178">Vendors and products can be grouped by territory, and different offers can be provided, depending on the country or region of the transaction.</span></span> <span data-ttu-id="3ffe5-179">Kai vartotojai pasirenka produktus, jie gali apibrėžti įtrauktas prekes ir prekių, kurios bus naudojamos grąžinimo sudengime, skaičių.</span><span class="sxs-lookup"><span data-stu-id="3ffe5-179">When users select products, they can define the items that are included and the number of items that will be used in the rebate settlement.</span></span>