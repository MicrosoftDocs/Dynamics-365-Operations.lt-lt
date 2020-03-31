---
title: Nuolaidos pagal mokėjimo būdą
description: Šioje temoje pateikiama funkcijų, kurios leidžia pardavėjams konfigūruoti nuolaidas pagal konkrečius mokėjimo būdus, apžvalga.
author: bebeale
manager: AnnBe
ms.date: 10/30/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Version 10.0.7
ms.openlocfilehash: 06de834d8081056fab6f628b24ec3eb1cb43d6f6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023389"
---
# <a name="tender-based-discounts"></a><span data-ttu-id="fea02-103">Nuolaidos pagal mokėjimo būdą</span><span class="sxs-lookup"><span data-stu-id="fea02-103">Tender-based discounts</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="fea02-104">Pardavėjai dažnai pristato privačias, firmines kredito korteles.</span><span class="sxs-lookup"><span data-stu-id="fea02-104">It's a common practice among retailers to release private, branded credit cards.</span></span> <span data-ttu-id="fea02-105">Pardavėjams tai yra naudinga, nes jiems bankai pasiūlo pageidaujamus tarifus.</span><span class="sxs-lookup"><span data-stu-id="fea02-105">The retailers benefit because they get preferred rates from the banks.</span></span> <span data-ttu-id="fea02-106">Be to, kadangi šios kredito kortelės gali paskatinti klientus dažniau apsilankyti parduotuvėje, jos padeda padidinti bendras pardavėjo pajamas.</span><span class="sxs-lookup"><span data-stu-id="fea02-106">Additionally, because these credits cards can encourage customers to visit the store more often, they help improve the retailer's bottom line.</span></span> <span data-ttu-id="fea02-107">Todėl pardavėjai yra suinteresuoti skatinti klientus naudoti firmines kredito korteles.</span><span class="sxs-lookup"><span data-stu-id="fea02-107">Therefore, retailers have an incentive to increase customer use of their branded credit cards.</span></span> <span data-ttu-id="fea02-108">Siekdami šio tikslo, jie dažnai teikia papildomas nuolaidas klientams, naudojantiems šias kredito korteles.</span><span class="sxs-lookup"><span data-stu-id="fea02-108">To achieve this goal, they often provide additional discounts to customers who use these credit cards.</span></span>

<span data-ttu-id="fea02-109">Be to, pardavėjai, kurie nesiūlo firminių kredito kortelių, gali skatinti klientus atsiskaityti kitais būdais, pvz., naudojant grynuosius pinigus, dovanų korteles ar lojalumo taškus.</span><span class="sxs-lookup"><span data-stu-id="fea02-109">Alternatively, retailers who don't provide branded credit cards might want to encourage customers to pay by using other tender types, such as cash, gift cards, or loyalty points.</span></span> <span data-ttu-id="fea02-110">Tokiu būdu jie gali sumažinti kredito kortelių aptarnavimo mokesčių išlaidas.</span><span class="sxs-lookup"><span data-stu-id="fea02-110">In this way, they can help reduce the expense of credit card processing fees.</span></span> <span data-ttu-id="fea02-111">Todėl pardavėjai gali teikti nuolaidas klientams, naudojantiems šiuos alternatyvius mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="fea02-111">Therefore, retailers might provide discounts to customers who use these alternative tender types.</span></span>

<span data-ttu-id="fea02-112">Dirbdami su „Microsoft Dynamics 365 Commerce“, pardavėjai gali konfigūruoti nuolaidos procentus, taikomus atitinkamoms eilutėms, jei klientas moka naudodamas pageidaujamą mokėjimo priemonės tipą.</span><span class="sxs-lookup"><span data-stu-id="fea02-112">In Microsoft Dynamics 365 Commerce, retailers can configure a discount percentage that is applied to qualified lines if the customer pays by using the preferred tender type.</span></span> <span data-ttu-id="fea02-113">Klientas gali pasirinkti atlikti dalinį arba pilną apmokėjimą, o „Commerce” nustato atitinkamą nuolaidos sumą.</span><span class="sxs-lookup"><span data-stu-id="fea02-113">The customer can decide whether to do a partial payment or a full payment, and Commerce determines the appropriate discount amount.</span></span> <span data-ttu-id="fea02-114">Atkreipkite dėmesį, kad nuolaida visada taikoma atitinkamų prekių sumai prieš mokesčius.</span><span class="sxs-lookup"><span data-stu-id="fea02-114">Note that the discount is always given on the pre-tax amount of the qualified items.</span></span>

<span data-ttu-id="fea02-115">Nuolaidos pagal mokėjimo būdą nekonkuruoja su nuolaidomis, susijusiomis su preke, pvz., periodinėmis arba neautomatinėmis nuolaidomis.</span><span class="sxs-lookup"><span data-stu-id="fea02-115">Tender-based discounts don't compete with item-based discounts, such as periodic or manual discounts.</span></span> <span data-ttu-id="fea02-116">Jos visada skaičiuojamos kartu su prekių nuolaidomis.</span><span class="sxs-lookup"><span data-stu-id="fea02-116">They are always compounded over the item discounts.</span></span> <span data-ttu-id="fea02-117">Todėl net jei prekei taikoma išskirtinė periodinė nuolaida, nuolaida pagal mokėjimo būdą vis tiek taikoma kartu su išskirtinėje periodine nuolaida.</span><span class="sxs-lookup"><span data-stu-id="fea02-117">Therefore, even if an exclusive periodic discount is applied to an item, the tender-based discount is still applied on top of the exclusive periodic discount.</span></span> <span data-ttu-id="fea02-118">Analogiškai, jei operacijai taikoma ribinė nuolaida, o nuolaida pagal mokėjimo būdą sumažina bendrą sumą iki mažesnės už ribinę vertės, operacijai vis tiek taikoma ribinė nuolaida.</span><span class="sxs-lookup"><span data-stu-id="fea02-118">Likewise, if a threshold discount is applied to the transaction, and the tender-based discount reduces the total below the threshold, the threshold discount is still applied to the transaction.</span></span>

<span data-ttu-id="fea02-119">Nors nuolaidos pagal mokėjimo būdą sumažina operacijos tarpinę sumą, tai neturi įtakos automatiniams mokesčiams, taikomiems operacijai.</span><span class="sxs-lookup"><span data-stu-id="fea02-119">Even though tender-based discounts reduce the subtotal of the transaction, automatic charges that are applied to the transaction aren't affected.</span></span> <span data-ttu-id="fea02-120">Pavyzdžiui, jei dėl to, kad tarpinė suma buvo didesnė nei 100 JAV dol., buvo apskaičiuotos 5 JAV dol. pristatymo išlaidos, o nuolaida pagal mokėjimo būdą sumažina sumą iki mažesnės nei 100 JAV dol., užsakymo pristatymo išlaidos vis tiek yra 5 JAV dol.</span><span class="sxs-lookup"><span data-stu-id="fea02-120">For example, if the delivery charges are calculated as $5 because the subtotal was more than $100, and the tender-based discount reduces the amount so that it's less than $100, the delivery charges are still $5 for the order.</span></span>


> [!NOTE]
> <span data-ttu-id="fea02-121">Nuolaidos pagal mokėjimo būdą proporcingai paskirstomos atitinkamoms pardavimo eilutėms ir sumažina atskirų eilučių sumą prieš mokesčius.</span><span class="sxs-lookup"><span data-stu-id="fea02-121">Tender-based discounts are proportionally distributed to the qualified sales lines and reduce the pre-tax amount of the individual lines.</span></span> <span data-ttu-id="fea02-122">Jei mokėjimo priemonės tipui yra sukonfigūruotos kelios nuolaidos pagal mokėjimo būdą (pavyzdžiui, grynaisiais pinigais), taikoma tik didžiausia nuolaida pagal mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="fea02-122">If multiple tender-based discounts are configured for a tender type (for example, cash), only the best tender-based discount is applied.</span></span>

<span data-ttu-id="fea02-123">Nuolaidas pagal mokėjimo būdą galima taikyti tik pardavimo eilutėms, kuriose kainos nėra užrakintos.</span><span class="sxs-lookup"><span data-stu-id="fea02-123">Tender-based discounts can be applied only to sales lines where the prices aren't locked.</span></span> <span data-ttu-id="fea02-124">Jei į užsakymą įtraukiamos naujos pardavimo eilutės, nuolaida pagal mokėjimo būdą taikoma naujoms pardavimo eilutėms tik mokėjimo metu.</span><span class="sxs-lookup"><span data-stu-id="fea02-124">If new sales lines are added to an order, the tender-based discount is applied to the new sales lines only during payment.</span></span> <span data-ttu-id="fea02-125">Tuo metu, kai pateikiamas kliento paėmimo arba siuntimo užsakymas, nuolaida pagal mokėjimo priemonę taikoma tik depozito sumai.</span><span class="sxs-lookup"><span data-stu-id="fea02-125">While a customer order for pickup or shipment is being placed, the tender-based discount is applied only to the deposit amount.</span></span> <span data-ttu-id="fea02-126">Pateikus užsakymą, vykdymo metu pardavimo eilučių kainos yra užrakintos.</span><span class="sxs-lookup"><span data-stu-id="fea02-126">After the order is placed, during fulfillment, the prices of the sales lines are locked.</span></span> <span data-ttu-id="fea02-127">Todėl jokia nuolaida pagal mokėjimo būdą netaikoma jokiam balansui, kuris apmokamas paėmimo metu arba autorizuojamas pristatymo metu.</span><span class="sxs-lookup"><span data-stu-id="fea02-127">Therefore, no tender-based discount is applied to any balance that is paid during pickup or authorized during shipment.</span></span> <span data-ttu-id="fea02-128">Nuolaida pagal mokėjimo būdą gali būti taikoma visai kliento užsakymo sumai tik tuo atveju, jei pardavėjas surenka visą sumą kaip depozitą užsakymo pateikimo metu.</span><span class="sxs-lookup"><span data-stu-id="fea02-128">The tender-based discount can be applied to the whole amount of a customer order only if the retailer collects the whole amount as a deposit while the order is being placed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fea02-129">Dirbant su „Commerce“, nuolaidos pagal mokėjimo būdą šiuo metu galimos dviem mokėjimo tipams: kredito kortele ir grynaisiais pinigais.</span><span class="sxs-lookup"><span data-stu-id="fea02-129">In Commerce, tender-based discounts are currently limited to two payment types: credit cards and cash.</span></span>

## <a name="pos-user-experience"></a><span data-ttu-id="fea02-130">EKA vartotojo patirtis</span><span class="sxs-lookup"><span data-stu-id="fea02-130">POS user experience</span></span>

<span data-ttu-id="fea02-131">Jei nuolaida pagal mokėjimo būda yra nustatyta gryniesiems pinigams, o kasininkas, dirbantis su elektroniniu kasos aparatu (EKA), pasirenka mygtuką, kuris yra susietas su mokėjimo grynaisiais operacija, nuolaida pagal mokėjimo būdą operacijai taikoma automatiškai.</span><span class="sxs-lookup"><span data-stu-id="fea02-131">If the tender-based discount is set up for cash, and the cashier at the point of sale (POS) selects a button that is mapped to the Pay cash operation, the tender-based discount is automatically applied to the transaction.</span></span> <span data-ttu-id="fea02-132">Tada sumažinta suma rodoma kaip balansas.</span><span class="sxs-lookup"><span data-stu-id="fea02-132">The reduced amount is then shown as the balance.</span></span> <span data-ttu-id="fea02-133">Tačiau, jei kasininkas pasirenka mokėjimo ekrano mygtuką **Atgal**, nuolaida bus pašalinta, o operacijos ekrane bus rodoma pradinė suma.</span><span class="sxs-lookup"><span data-stu-id="fea02-133">However, if the cashier selects the **Back** button on the payment screen, the discount is removed, and the original amount is shown on the transaction screen.</span></span> <span data-ttu-id="fea02-134">Jei mokėjimo eilutė tuščia, nuolaida pagal mokėjimo būdą pašalinama.</span><span class="sxs-lookup"><span data-stu-id="fea02-134">The tender-based discount is removed if the payment line is voided.</span></span>

<span data-ttu-id="fea02-135">Mokant kortele, pardavėjai gali nustatyti nuolaidą pagal mokėjimo būdą vienam ar daugiau kredito kortelių tipų.</span><span class="sxs-lookup"><span data-stu-id="fea02-135">For cards payments, retailers can set the tender-based discount on one or more types of credit cards.</span></span> <span data-ttu-id="fea02-136">Tačiau sistema negali patikrinti naudojamos kredito kortelės tipo, jei kortelė nėra autorizuota.</span><span class="sxs-lookup"><span data-stu-id="fea02-136">However, the system can't verify the type of credit card that is used unless the card is authorized.</span></span> <span data-ttu-id="fea02-137">Jei nuolaida taikoma po autorizavimo, mokėjimo autorizavimas bus taikomas didesnei sumai, o mokėjimo fiksavimas bus taikomas mažesnei sumai.</span><span class="sxs-lookup"><span data-stu-id="fea02-137">If the discount is applied after authorization, the payment authorization will be for a larger amount, but the payment capture will be for a smaller amount.</span></span>

<span data-ttu-id="fea02-138">Siekiant išvengti šios situacijos, jei klientas moka kredito kortele, kasininkas mato dialogo langą, kuriame rodomos kredito kortelės, leisiančios klientui sutaupyti papildomai.</span><span class="sxs-lookup"><span data-stu-id="fea02-138">To help prevent this situation, if a customer pays with a credit card, the cashier sees a dialog box that lists credit cards that will bring the customer additional savings.</span></span> <span data-ttu-id="fea02-139">Kasininkas gali paklausti, ar klientas nori naudoti vieną iš pageidaujamų kortelių papildomai nuolaidai gauti.</span><span class="sxs-lookup"><span data-stu-id="fea02-139">The cashier can then ask whether the customer wants to use one of the preferred cards to get an additional discount.</span></span> <span data-ttu-id="fea02-140">Jei kasininkas naudoja pageidaujamą kortelę, nuolaida pagal mokėjimo būdą taikoma operacijai, o sumažinta suma rodoma mokėjimo ekrane.</span><span class="sxs-lookup"><span data-stu-id="fea02-140">If the cashier uses a preferred card, the tender-based discount is applied to the transaction, and the reduced amount is shown on the payment screen.</span></span> <span data-ttu-id="fea02-141">Autorizavimas bus taikomas sumažintai sumai.</span><span class="sxs-lookup"><span data-stu-id="fea02-141">The authorization will be for the reduced amount.</span></span> <span data-ttu-id="fea02-142">Jei klientas naudoja kortelę, kuri skiriasi nuo kortelės, kurią pasirinko kasininkas, rodomas klaidos pranešimas ir autorizavimas nebegalioja.</span><span class="sxs-lookup"><span data-stu-id="fea02-142">If the customer inserts a card that differs from the card that the cashier selected, an error message is shown, and the authorization is voided.</span></span>


## <a name="call-center-user-experience"></a><span data-ttu-id="fea02-143">Skambučių centro vartotojo patirtis</span><span class="sxs-lookup"><span data-stu-id="fea02-143">Call center user experience</span></span>

<span data-ttu-id="fea02-144">Kai skambučių centro užsakymo metu vartotojas pasirenka **Baigti**, rodomas ekranas **Sumos**.</span><span class="sxs-lookup"><span data-stu-id="fea02-144">When the user selects **Complete** during a call center order, the **Totals** screen is shown.</span></span> <span data-ttu-id="fea02-145">Iš pradžių šio ekrano sumos neapima nuolaidų pagal mokėjimo būdą, nes dar nepasirinktas mokėjimo būdas.</span><span class="sxs-lookup"><span data-stu-id="fea02-145">At first, the totals on this screen don't include tender-based discounts, because the payment method hasn't yet been selected.</span></span> <span data-ttu-id="fea02-146">Ekrane **Įtraukti mokėjimą**, jei vartotojas pasirenka mokėjimo būdą, kuriam yra sukonfigūruota nuolaida pagal mokėjimo būdą, mokėjimo suma automatiškai koreguojama, kad atitiktų sumą su nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="fea02-146">On the **Add payment** screen, if the user selects the payment method that the tender-based discount is configured for, the payment amount is automatically adjusted so that it reflects the discounted amount.</span></span> <span data-ttu-id="fea02-147">Kaip ir EKA kliento atveju, skambučių centro klientas gali nuspręsti, ar atlikti pilną mokėjimą, ar dalinį mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="fea02-147">Like the customer at the POS, the call center customer can decide whether to pay the full payment or a partial payment.</span></span> <span data-ttu-id="fea02-148">Remiantis sumokėta suma, pardavimo užsakymui taikoma nuolaida pagal mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="fea02-148">Based on the amount that is paid, the tender-based discount is applied to the sales order.</span></span>

> [!NOTE]
> <span data-ttu-id="fea02-149">Skambučių centro užsakymams kortelių tikrinimas nėra atliekamas.</span><span class="sxs-lookup"><span data-stu-id="fea02-149">Card validation isn't done for call center orders.</span></span> <span data-ttu-id="fea02-150">Pavyzdžiui, jei skambučių centro vartotojas pasirenka „Visa“ kredito kortelę, tačiau klientas naudoja „Mastercard“, sistema vis tiek taiko nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="fea02-150">For example, if the call center user selects Visa as the credit card, but the customer uses Mastercard, the system still applies the discount.</span></span>

## <a name="exclude-items-from-discounts"></a><span data-ttu-id="fea02-151">Netaikyti nuolaidų prekėms</span><span class="sxs-lookup"><span data-stu-id="fea02-151">Exclude items from discounts</span></span>

<span data-ttu-id="fea02-152">Pardavėjai dažnai pasirenka netaikyti nuolaidų kai kuriems produktams, pvz., naujoms prekėms arba paklausioms prekėms.</span><span class="sxs-lookup"><span data-stu-id="fea02-152">Retailers often choose to exclude some products, such as new items or in-demand items, from discounts.</span></span> <span data-ttu-id="fea02-153">Tačiau jie vis dar gali norėti taikyti nuolaidas pagal mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="fea02-153">However, they might still want to apply tender-based discounts.</span></span> <span data-ttu-id="fea02-154">Pavyzdžiui, pardavėjas gali sukonfigūruoti „Commerce“, kad nebūtų taikomos su preke susijusios nuolaidos arba neautomatinės nuolaidos.</span><span class="sxs-lookup"><span data-stu-id="fea02-154">For example, a retailer configures Commerce so that it doesn't allow item-based discounts or manual discounts.</span></span> <span data-ttu-id="fea02-155">Tačiau, jei klientas moka naudodamas pageidaujamą mokėjimo priemonę, „Commerce“ vis dar taiko nuolaidą pagal mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="fea02-155">However, if the customer pays by using the preferred tender, Commerce still applies the tender-based discount.</span></span> <span data-ttu-id="fea02-156">Norėdami nustatyti „Commerce“ šiuo būdu, pardavėjai turi eiti į **Produkto informacijos valdymas > Produktai > Išleisti produktai**, pasirinkti prekę, tada „FastTab“ **Commerce** parinktis **Neleisti jokių nuolaidų** ir **Neleisti mokėjimo priemone pagrįstų nuolaidų** nustatyti į **Ne**, o parinktis **Neleisti nuolaidų** ir **Neleisti rankiniu būdu įvedamų nuolaidų** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="fea02-156">To set up Commerce in this manner, retailers must go to **Product information management > Products > Released products**, select the item, and then, on the **Commerce** FastTab, set the **Prevent all discounts** and **Prevent tender based discounts** options to **No**, and the **Prevent discounts** and **Prevent manual discounts** options to **Yes**.</span></span>

> [!NOTE]
> <span data-ttu-id="fea02-157">Kaip konfigūracija **Neleisti jokių nuolaidų** nustatyta į **Taip**, produktui nebus taikoma jokių nuolaidų.</span><span class="sxs-lookup"><span data-stu-id="fea02-157">When the **Prevent all discounts** configuration is set to **Yes**, no discounts will be applied to the product.</span></span> <span data-ttu-id="fea02-158">Nebus taikomos netgi nuolaidos pagal mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="fea02-158">Not even tender-based discounts will be applied.</span></span>