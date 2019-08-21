---
title: Mokėjimo nuolaidos
description: Mokėjimo nuolaidos yra nustatomos ir bendrai naudojamos dalyse Mokėtinos sumos ir Gautinos sumos.  Galimą mokėjimo nuolaidą galima nurodyti kliento SF arba tiekėjo SF; ji bus pritaikyta, jei sąskaita faktūra bus apmokėta mokėjimo nuolaidos laikotarpiu.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 139fb4fdb7d4f8034bff5e9668dc794f29fb327e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842553"
---
# <a name="cash-discounts"></a><span data-ttu-id="32e29-104">Mokėjimo nuolaidos</span><span class="sxs-lookup"><span data-stu-id="32e29-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32e29-105">Mokėjimo nuolaidos yra nustatomos ir bendrai naudojamos dalyse Mokėtinos sumos ir Gautinos sumos.</span><span class="sxs-lookup"><span data-stu-id="32e29-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="32e29-106">Galimą mokėjimo nuolaidą galima nurodyti kliento SF arba tiekėjo SF; ji bus pritaikyta, jei sąskaita faktūra bus apmokėta mokėjimo nuolaidos laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="32e29-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="32e29-107">Mokėjimo nuolaidos</span><span class="sxs-lookup"><span data-stu-id="32e29-107">Cash discounts</span></span>

<span data-ttu-id="32e29-108">Tiek klientų, tiek tiekėjų mokėjimo nuolaidas galima kurti Mokėjimo nuolaidų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="32e29-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="32e29-109">Taip pat naudodami Kito nuolaidos kodo lauką galite apibrėžti mokėjimo nuolaidų seką, kuri pradedama taikyti baigiant galioti ankstesnėms mokėjimo nuolaidų datoms.</span><span class="sxs-lookup"><span data-stu-id="32e29-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="32e29-110">Daugiau informacijos rasite toliau šioje temoje, „Pavyzdys: mokėjimo nuolaidų seka‟.</span><span class="sxs-lookup"><span data-stu-id="32e29-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="32e29-111">Jei SF, kredito operacija (mokėjimas arba kredito pažyma), arba jos abi įvedamos valiuta, kuri skiriasi nuo juridinio subjekto apskaitos valiutos, mokėjimo nuolaida apskaičiuojama naudojant mokėjimo arba kredito pažymos dienos valiutos kursą.</span><span class="sxs-lookup"><span data-stu-id="32e29-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="32e29-112">Jei SF ir kredito dokumentas įvedami skirtinguose juridiniuose subjektuose, ir jei skiriasi juridinių subjektų apskaitos valiutos, kredito dokumento dienos valiutos kursas paimamas iš SF juridinio subjekto.</span><span class="sxs-lookup"><span data-stu-id="32e29-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="32e29-113">Daugiau informacijos rasite toliau šioje temoje, „Pavyzdys: mokėjimo nuolaidų valiutos kursai‟.</span><span class="sxs-lookup"><span data-stu-id="32e29-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="32e29-114">Numatytasis mokėjimo nuolaidos pagrindinės sąskaitos užsakymo apdorojimas</span><span class="sxs-lookup"><span data-stu-id="32e29-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="32e29-115">Jei, norint gauti mokėjimo nuolaidą, SF sudengiama laiku, mokėjimo nuolaida automatiškai registruojama mokėjimo nuolaidos pagrindinėje sąskaitoje pagal toliau nurodytą numatytąjį prioritetą.</span><span class="sxs-lookup"><span data-stu-id="32e29-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="32e29-116">Pagrindinė sąskaita, nurodyta lauke Alternatyvi mokėjimo nuolaidos sąskaita, esančiame klientų puslapyje Sudengti atidarytas operacijas arba tiekėjų puslapyje Sudengti atidarytas operacijas.</span><span class="sxs-lookup"><span data-stu-id="32e29-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="32e29-117">Pagrindinė sąskaita, nurodyta DK registravimo grupės, priskirtos SF PVM grupei, lauke Kliento mokėjimo nuolaida arba lauke Tiekėjo mokėjimo nuolaida.</span><span class="sxs-lookup"><span data-stu-id="32e29-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="32e29-118">DK registravimo grupes nustatykite DK registravimo grupių puslapyje ir jas priskirkite PVM kodams PVM kodų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="32e29-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="32e29-119">Mokėjimo nuolaidos kodo, esančio sudengtoje SF, pagrindinė registravimo sąskaita Mokėjimo nuolaidų puslapio lauke Pagrindinė sąskaita, skirta kliento nuolaidoms arba lauke Pagrindinė sąskaita, skirta tiekėjo nuolaidoms.</span><span class="sxs-lookup"><span data-stu-id="32e29-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="32e29-120">Pagrindinė mokėjimo nuolaidų sąskaita, kaip apibrėžta Automatinių operacijų sąskaitų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="32e29-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="32e29-121"> Pavyzdys: mokėjimo nuolaidų seka</span><span class="sxs-lookup"><span data-stu-id="32e29-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="32e29-122">Nustatykite tris mokėjimo nuolaidos kodus:</span><span class="sxs-lookup"><span data-stu-id="32e29-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="32e29-123">Kodas 5D10% – 10 proc. mokėjimo nuolaida, jei suma sumokama per 5 dienas.</span><span class="sxs-lookup"><span data-stu-id="32e29-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="32e29-124">Kodas 10D5% – 5 proc. mokėjimo nuolaida, jei suma sumokama per 10 dienų.</span><span class="sxs-lookup"><span data-stu-id="32e29-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="32e29-125">Kodas 14D2% – 2 proc. mokėjimo nuolaida, jei suma sumokama per 14 dienų.</span><span class="sxs-lookup"><span data-stu-id="32e29-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="32e29-126">Lauke Kitas nuolaidos kodas:</span><span class="sxs-lookup"><span data-stu-id="32e29-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="32e29-127">Kodui 5D10% pasirinkite 10D5%.</span><span class="sxs-lookup"><span data-stu-id="32e29-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="32e29-128">Kodui 10D5% pasirinkite 14D2%.</span><span class="sxs-lookup"><span data-stu-id="32e29-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="32e29-129">Pasirinkę kodą 14D2%, lauką Naujas nuolaidos kodas palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="32e29-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="32e29-130">Mokėjimo datai esant vėlesnei už ankstesnę SF mokėjimo nuolaidos datą, viena po kitos taikomos šios trys mokėjimo nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="32e29-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="32e29-131">Apmokėjus SF, suteikiama tik viena mokėjimo nuolaida – pagal tai, kuri mokėjimo nuolaidų sekos data patenkinama.</span><span class="sxs-lookup"><span data-stu-id="32e29-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="32e29-132"> Pavyzdys: mokėjimo nuolaidų valiutų kursai</span><span class="sxs-lookup"><span data-stu-id="32e29-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="32e29-133">Jūsų juridinio subjekto apskaitos valiuta yra EUR, o toliau pateikti valiutų kursai nurodyti USD.</span><span class="sxs-lookup"><span data-stu-id="32e29-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="32e29-134">Vasario 1 d. = 110.</span><span class="sxs-lookup"><span data-stu-id="32e29-134">February 1 = 110</span></span>
-   <span data-ttu-id="32e29-135">Kovo 1 d. = 80.</span><span class="sxs-lookup"><span data-stu-id="32e29-135">March 1 = 80</span></span>

<span data-ttu-id="32e29-136">1000 USD SF su 20D2% mokėjimo nuolaidos sąlygomis užregistruojama vasario 15 d.</span><span class="sxs-lookup"><span data-stu-id="32e29-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="32e29-137">SF apskaitos valiutos suma yra 1100 EUR.</span><span class="sxs-lookup"><span data-stu-id="32e29-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="32e29-138">980 USD mokėjimas su SF sudengiamas kovo 1 d.</span><span class="sxs-lookup"><span data-stu-id="32e29-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="32e29-139">Mokėjimo nuolaidos suma yra 20 USD.</span><span class="sxs-lookup"><span data-stu-id="32e29-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="32e29-140">Mokėjimo apskaitos valiutos suma yra 784 EUR.</span><span class="sxs-lookup"><span data-stu-id="32e29-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="32e29-141">Mokėjimo nuolaidos apskaitos valiutos suma apskaičiuojama naudojant kovo 1 d. valiutos kursą: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="32e29-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="32e29-142">Jei Gautinų sumų parametrų ar Mokėtinų sumų parametrų puslapiuose pasirinkta parinktis Skaičiuoti dalinių mokėjimų mokėjimo nuolaidas, naudojamas kiekvieno dalinio mokėjimo dieną galiojantis valiutos kursas.</span><span class="sxs-lookup"><span data-stu-id="32e29-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 

