---
title: "Kredito kortelių nustatymas, autorizacija ir patvirtinimas"
description: "Šiame straipsnyje pateikiama kredito kortelės autorizavimo programoje „Microsoft Dynamics 365 for Finance and Operations“ apžvalga. Jame pateikiama informacija apie tai, kaip nustatyti mokėjimo tarnybą, į pardavimo užsakymą įtraukti kredito kortelę ir anuliuoti autorizaciją."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5a950a100fd5e9026300ea08eb1a6311a8e63129
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="cad28-104">Kredito kortelių nustatymas, autorizacija ir patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="cad28-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="cad28-105">Šiame straipsnyje pateikiama kredito kortelės autorizavimo programoje „Microsoft Dynamics 365 for Finance and Operations“ apžvalga.</span><span class="sxs-lookup"><span data-stu-id="cad28-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="cad28-106">Jame pateikiama informacija apie tai, kaip nustatyti mokėjimo tarnybą, į pardavimo užsakymą įtraukti kredito kortelę ir anuliuoti autorizaciją.</span><span class="sxs-lookup"><span data-stu-id="cad28-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="cad28-107">Kredito kortelės mokėjimo paslaugos nustatymas</span><span class="sxs-lookup"><span data-stu-id="cad28-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="cad28-108">Norėdami naudotis kredito kortelėmis, turite sukurti ir aktyvuoti mokėjimo paslaugą Mokėjimo paslaugų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="cad28-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="cad28-109">Mokėjimo paslauga veikia kaip tiltas, jungiantis jūsų organizaciją su klientų kreditinių kortelių mokėjimus apdorojančiu banku.</span><span class="sxs-lookup"><span data-stu-id="cad28-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="cad28-110">Turite dirbti su kredito kortelių teikėju, nurodytu mokėjimo jungties lauke ir sukurti sąskaitą su tuo teikėju.</span><span class="sxs-lookup"><span data-stu-id="cad28-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="cad28-111">Tada turite sukurti kitas parinktis Mokėjimo paslaugų puslapyje, nustatyti kredito kortelių rūšis, skirtas „American Express“, „Discover“, „MasterCard“ ir „Discover“ Kredito kortelių rūšių puslapyje, ir aktyvuoti teikėją kaip numatytąjį teikėją.</span><span class="sxs-lookup"><span data-stu-id="cad28-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="cad28-112">Taip pat, norėdami baigti sąranką, turite atlikti šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="cad28-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="cad28-113">Gautinų sumų parametrų puslapyje nurodykite parametrus, naudotinus kreditinių kortelių autorizavimui.</span><span class="sxs-lookup"><span data-stu-id="cad28-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="cad28-114">Mokėjimo sąlygų puslapyje nustatykite kredito kortelės mokėjimo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="cad28-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="cad28-115">Mokėjimo tipo lauke pasirinkite Kreditinę kortelę.</span><span class="sxs-lookup"><span data-stu-id="cad28-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="cad28-116">Kliento kredito kortelių puslapyje įveskite kredito kortelės informaciją klientams.</span><span class="sxs-lookup"><span data-stu-id="cad28-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="cad28-117">Kaip pridėti naują kreditinę kortelę</span><span class="sxs-lookup"><span data-stu-id="cad28-117">Adding a new credit card</span></span>
<span data-ttu-id="cad28-118">Naujos kredito kortelės duomenis galite sukurti Klientų puslapyje naudodami Klientas, Nustatyti, Kreditinė kortelė.</span><span class="sxs-lookup"><span data-stu-id="cad28-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="cad28-119">Taip pat galite sukurti kreditinių kortelių įrašus, įvesdami pardavimų užsakymus Pardavimų užsakymų puslapyje, naudodami Tvarkyti, Klientas, Kreditinė kortelė, Registruoti.</span><span class="sxs-lookup"><span data-stu-id="cad28-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>
<span data-ttu-id="cad28-120">Kaip pridėti kreditinę kortelę pardavimo užsakymui</span><span class="sxs-lookup"><span data-stu-id="cad28-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="cad28-121">Galite pridėti kreditinę kortelę pardavimo užsakymui, pasirinkdami kredito kortelę iš kredito kortelių paieškos iš Kainų ir nuolaidų „FastTab“ Pardavimų užsakymo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="cad28-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="cad28-122">Norėdami pradėti autorizavimo procesą, Veiksmų srityje, Tvarkyti kortelę, pasirinkite Kredito kortelė ir Autorizuoti.</span><span class="sxs-lookup"><span data-stu-id="cad28-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>
<span data-ttu-id="cad28-123">Kredito kortelės autorizacija</span><span class="sxs-lookup"><span data-stu-id="cad28-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="cad28-124">Autorizavus kredito kortelę, patikrinamas kortelės numeris ir kortelės savininko vardas ir patvirtinamas turimas kredito likutis.</span><span class="sxs-lookup"><span data-stu-id="cad28-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="cad28-125">Pasirinktinai tikrinama kortelės patvirtinimo vertė ir kortelės savininko adresas.</span><span class="sxs-lookup"><span data-stu-id="cad28-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="cad28-126">Kliento turimas kredito likutis sumažinamas pardavimo sąskaitoje faktūroje nurodyta suma.</span><span class="sxs-lookup"><span data-stu-id="cad28-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="cad28-127">Mokėjimo paslauga siunčia informaciją, kad kredito kortelė buvo patvirtinta arba atmesta.</span><span class="sxs-lookup"><span data-stu-id="cad28-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="cad28-128">Pardavimo pavedimi išrašius sąskaitą, sąskaitos faktūros suma nurašoma iš kredito kortelės.</span><span class="sxs-lookup"><span data-stu-id="cad28-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="cad28-129">Kortelės tikrinimo vertė</span><span class="sxs-lookup"><span data-stu-id="cad28-129">Card verification value</span></span>

<span data-ttu-id="cad28-130">Galite reikalauti kortelės patvirtinimo vertės, kuri kartais vadinama kortelės apsaugos kodu.</span><span class="sxs-lookup"><span data-stu-id="cad28-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="cad28-131">„American Express“ kortelėms tai keturių skaitmenų reikšmė.</span><span class="sxs-lookup"><span data-stu-id="cad28-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="cad28-132">„Discover“, „MasterCard“ ir „Visa“ kortelėms šis skaičius yra triženklis.</span><span class="sxs-lookup"><span data-stu-id="cad28-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="cad28-133">Adreso tikrinimas</span><span class="sxs-lookup"><span data-stu-id="cad28-133">Address verification</span></span>

<span data-ttu-id="cad28-134">Adreso patikrinimo informacija visada siunčiama mokėjimo paslaugų teikėjui.</span><span class="sxs-lookup"><span data-stu-id="cad28-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="cad28-135">Galite nuspręsti, kiek informacijos reikia, kad operacija būtų priimta.</span><span class="sxs-lookup"><span data-stu-id="cad28-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="cad28-136">Būtinai pasitikrinkite, ar jūsų teikėjas priima šią informaciją.</span><span class="sxs-lookup"><span data-stu-id="cad28-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="cad28-137">Adreso patvirtinimo variantai yra šie:</span><span class="sxs-lookup"><span data-stu-id="cad28-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="cad28-138">**Visada priimti sandorį** – priimti sandorį, neatsižvelgiant į adreso patikrinimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="cad28-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="cad28-139">**Sąskaitos turėtojas** – palyginti kortelės savininko vardą iš sandorio su kredito kortelės įmonės informacija.</span><span class="sxs-lookup"><span data-stu-id="cad28-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="cad28-140">**Atsiskaitymo adresas** – palyginti kortelės savininko vardą ir atsiskaitymo adresą iš sandorio su kredito kortelės įmonės informacija.</span><span class="sxs-lookup"><span data-stu-id="cad28-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="cad28-141">**Atsiskaitymo pašto kodas** – palyginti kortelės savininko vardą, pavardę, atsiskaitymo adresą ir pašto kodą iš sandorio su kredito kortelės įmonės informacija.</span><span class="sxs-lookup"><span data-stu-id="cad28-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="cad28-142">Duomenų palaikymas</span><span class="sxs-lookup"><span data-stu-id="cad28-142">Data support</span></span>
<span data-ttu-id="cad28-143">Kiekvienam palaikomam kredito kortelės tipui galite nurodyti duomenų palaikymo lygį.</span><span class="sxs-lookup"><span data-stu-id="cad28-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="cad28-144">Lygis nurodo, kiek informacijos apie sandorį perduodama mokėjimo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="cad28-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="cad28-145">Būtinai paklauskite savo paslaugų teikėjo, ar jis gali suteikti šią informaciją.</span><span class="sxs-lookup"><span data-stu-id="cad28-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="cad28-146">Duomenų palaikymo lygio variantai yra šie:</span><span class="sxs-lookup"><span data-stu-id="cad28-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="cad28-147">**1 lygis** – perduoti sandorio datą, sandorio vertę ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="cad28-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="cad28-148">**2 lygis** – perduoti visą 1 lygio informaciją, siuntimo ir prekybininko adresus, ir informaciją apie mokesčius.</span><span class="sxs-lookup"><span data-stu-id="cad28-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="cad28-149">**3 lygis** – perduoti visą 2 lygio informaciją, siuntimo ir prekybininko adresus bei užsakymo eilutės informaciją.</span><span class="sxs-lookup"><span data-stu-id="cad28-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="cad28-150">Daliniai mokėjimai</span><span class="sxs-lookup"><span data-stu-id="cad28-150">Partial payments</span></span>
<span data-ttu-id="cad28-151">Jei gabenate dalį užsakymo, fiksuojama dalinio užsakymo suma, o autorizacija visai užsakymo sumai uždaroma.</span><span class="sxs-lookup"><span data-stu-id="cad28-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="cad28-152">Tada pateikiama nauja autorizacija likusio neišsiųsto užsakymo sumai.</span><span class="sxs-lookup"><span data-stu-id="cad28-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="cad28-153">Autorizavimo anuliavimas </span><span class="sxs-lookup"><span data-stu-id="cad28-153">Voiding an authorization</span></span>
<span data-ttu-id="cad28-154">Norėdami anuliuoti kreditinių kortelių autorizavimą, galite pakeisti mokėjimo būdą į kitą metodą, kuris neturi kredito kortelės tipo.</span><span class="sxs-lookup"><span data-stu-id="cad28-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>






