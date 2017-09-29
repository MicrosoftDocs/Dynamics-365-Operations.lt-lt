---
title: "Einamoji vidutinė savikaina"
description: "Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 875325bca949c0f3dfc0eab55f64db5659a2faef
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="running-average-cost-price"></a><span data-ttu-id="3ea67-104">Einamoji vidutinė savikaina</span><span class="sxs-lookup"><span data-stu-id="3ea67-104">Running average cost price</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="3ea67-105">Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje.</span><span class="sxs-lookup"><span data-stu-id="3ea67-105">The inventory close process settles issue transactions to receipt transactions, based on the inventory valuation method that is selected in the item’s item model group.</span></span> <span data-ttu-id="3ea67-106">Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="3ea67-106">However, before inventory close is run, the system calculates a running average cost price that is typically used when issue transactions are posted.</span></span>

<span data-ttu-id="3ea67-107">Sistema įvertina šią prekės naudojamą savikainą naudodama toliau pateiktą formulę.</span><span class="sxs-lookup"><span data-stu-id="3ea67-107">The system estimates this running average cost price for an item by using the following formula:</span></span> 

<span data-ttu-id="3ea67-108">Įvertinta kaina = (Faktinė suma + Finansinė suma) ÷ (Faktinis kiekis + Finansinis kiekis)</span><span class="sxs-lookup"><span data-stu-id="3ea67-108">Estimated price = (Physical amount + Financial amount) ÷ (Physical quantity + Financial quantity)</span></span>

## <a name="using-the-running-average-cost-price"></a><span data-ttu-id="3ea67-109">Einamosios vidutinės savikainos naudojimas</span><span class="sxs-lookup"><span data-stu-id="3ea67-109">Using the running average cost price</span></span>
<span data-ttu-id="3ea67-110">Šioje lentelėje rodoma, kai sistema užregistruoja atsargų operacijas naudodama einamąją vidutinę savikainą, ir kai naudojama savikaina, nustatyta prekės pagrindiniame įraše.</span><span class="sxs-lookup"><span data-stu-id="3ea67-110">The following table shows when the system posts inventory transactions by using the running average cost price, and when it uses the cost price that is defined on the item master record instead.</span></span>

| <span data-ttu-id="3ea67-111">Sąlyga</span><span class="sxs-lookup"><span data-stu-id="3ea67-111">Condition</span></span>                                               | <span data-ttu-id="3ea67-112">Sistema naudoja įvertintą einamąją vidutinę savikainą.</span><span class="sxs-lookup"><span data-stu-id="3ea67-112">The system uses the estimated running average cost price</span></span> | <span data-ttu-id="3ea67-113">Sistema naudoja savikainą, nustatytą prekės pagrindiniame įraše.</span><span class="sxs-lookup"><span data-stu-id="3ea67-113">The system uses the cost price that is defined on the item master</span></span> |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="3ea67-114">Ir skaitiklis\*, ir vardiklis\*\* yra teigiami.</span><span class="sxs-lookup"><span data-stu-id="3ea67-114">Both the numerator\* and denominator\*\* are positive.</span></span>  | <span data-ttu-id="3ea67-115">Taip</span><span class="sxs-lookup"><span data-stu-id="3ea67-115">Yes</span></span>                                                      | <span data-ttu-id="3ea67-116">Nr.</span><span class="sxs-lookup"><span data-stu-id="3ea67-116">No</span></span>                                                                |
| <span data-ttu-id="3ea67-117">Skaitiklis\*, vardiklis\*\* arba abu yra neigiami.</span><span class="sxs-lookup"><span data-stu-id="3ea67-117">The numerator\*, denominator\*\*, or both are negative.</span></span> | <span data-ttu-id="3ea67-118">Nr.</span><span class="sxs-lookup"><span data-stu-id="3ea67-118">No</span></span>                                                       | <span data-ttu-id="3ea67-119">Taip</span><span class="sxs-lookup"><span data-stu-id="3ea67-119">Yes</span></span>                                                               |
| <span data-ttu-id="3ea67-120">Vardiklis\*\* yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="3ea67-120">The denominator\*\* is 0 (zero).</span></span>                        | <span data-ttu-id="3ea67-121">Nr.</span><span class="sxs-lookup"><span data-stu-id="3ea67-121">No</span></span>                                                       | <span data-ttu-id="3ea67-122">Taip</span><span class="sxs-lookup"><span data-stu-id="3ea67-122">Yes</span></span>                                                               |

<span data-ttu-id="3ea67-123">\* Skaitiklis = (Faktinė suma + Finansinė suma) \*\* Vardiklis = (Faktinis kiekis + Finansinis kiekis)</span><span class="sxs-lookup"><span data-stu-id="3ea67-123">\* Numerator = (Physical amount + Financial amount) \*\* Denominator = (Physical quantity + Financial quantity)</span></span> 

<span data-ttu-id="3ea67-124">**Pastaba.** Jei prekės parinktis **Įtraukti faktinę vertę** nepasirinkta, sistema taiko 0 (nulis) ir faktinei sumai, ir faktiniam kiekiui.</span><span class="sxs-lookup"><span data-stu-id="3ea67-124">**Note:** If the **Include physical value** option isn't selected for an item, the system uses 0 (zero) for both the physical amount and the physical quantity.</span></span> <span data-ttu-id="3ea67-125">Informacijos apie šią parinktį rasite [Įtraukti faktinę vertę](include-physical-value.md).</span><span class="sxs-lookup"><span data-stu-id="3ea67-125">For information about this option, see [Include physical value](include-physical-value.md).</span></span>

## <a name="avoiding-pricing-amplification"></a><span data-ttu-id="3ea67-126">Kainos nepadidinimas</span><span class="sxs-lookup"><span data-stu-id="3ea67-126">Avoiding pricing amplification</span></span>
<span data-ttu-id="3ea67-127">Retais atvejais sistema įkainoja kelis išdavimus neturėdama pakankamai gavimų kainai pagrįsti.</span><span class="sxs-lookup"><span data-stu-id="3ea67-127">On rare occasions, the system prices several issues before it has enough receipts to base the price on.</span></span> <span data-ttu-id="3ea67-128">Tokiu atveju įvertinta einamoji vidutinė savikaina gali būti nustatoma per didelė.</span><span class="sxs-lookup"><span data-stu-id="3ea67-128">This scenario can cause estimates of the running average cost price to be overly inflated.</span></span> <span data-ttu-id="3ea67-129">Tačiau yra veiksmų, kuriuos galite atlikti, kad išvengtumėte kainos padidinimo, arba sumažintumėte jo poveikį jam įvykus.</span><span class="sxs-lookup"><span data-stu-id="3ea67-129">However, there are steps that you can take to avoid pricing amplification, or to reduce its impact when it does occur.</span></span> <span data-ttu-id="3ea67-130">**Scenarijus** Su preke, kuriai parinkote parinktį **Įtraukti faktinę vertę**, atliekamos tolesnės operacijos.</span><span class="sxs-lookup"><span data-stu-id="3ea67-130">**Scenario** The following transactions occur for an item that you've selected the **Include physical value** option for:</span></span>

1.  <span data-ttu-id="3ea67-131">Finansiškai gaunate kiekį 100, po 100,00 USD.</span><span class="sxs-lookup"><span data-stu-id="3ea67-131">You financially receive a quantity of 100 at USD 100.00.</span></span>
2.  <span data-ttu-id="3ea67-132">Finansiškai išduodate kiekį 200.</span><span class="sxs-lookup"><span data-stu-id="3ea67-132">You financially issue a quantity of 200.</span></span>
3.  <span data-ttu-id="3ea67-133">Faktiškai gaunate kiekį 101, po 202,00 USD.</span><span class="sxs-lookup"><span data-stu-id="3ea67-133">You physically receive a quantity of 101 at USD 202.00.</span></span>

<span data-ttu-id="3ea67-134">Tikrindami įvertintą einamąją vidutinę prekės savikainą, tikitės, kad ji bus 1,51 USD.</span><span class="sxs-lookup"><span data-stu-id="3ea67-134">When you examine the estimated running average cost price for the item, you expect a cost price of USD 1.51.</span></span> <span data-ttu-id="3ea67-135">Tačiau matote, kad įvertinta einamoji vidutinė savikaina yra 102,00 USD, apskaičiuota pagal šią formulę: įvertinta kaina = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102. Kaina taip padidėja dėl to, kad, kai 2 veiksmu finansiškai išduodama 200 prekių, 100 iš jų sistema turi įkainoti dar neturėdama atitinkamų gavimų.</span><span class="sxs-lookup"><span data-stu-id="3ea67-135">Instead, you find an estimated running average of USD 102.00, which is based on the following formula: Estimated price = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 This pricing amplification occurs because, when 200 items are issued financially in step 2, the system must price 100 of the items before it has any corresponding receipts.</span></span> <span data-ttu-id="3ea67-136">Dėl tokios situacijos atsargos tampa neigiamos.</span><span class="sxs-lookup"><span data-stu-id="3ea67-136">This situation causes negative inventory.</span></span> <span data-ttu-id="3ea67-137">Kaip galima tikėtis, tada sistema vieneto kainą įvertina 1,00 USD.</span><span class="sxs-lookup"><span data-stu-id="3ea67-137">The system then estimates a unit price of USD 1.00, as we might expect.</span></span> <span data-ttu-id="3ea67-138">Tačiau, gavus atitinkamus 100 gavimų, kiekvieno jų kaina yra 2,00 USD.</span><span class="sxs-lookup"><span data-stu-id="3ea67-138">However, when the corresponding 100 receipts arrive, they are at a unit price of USD 2.00 each.</span></span> 

<span data-ttu-id="3ea67-139">**Pastaba.** Nors dėl išdavimų sukuriamas neigiamas atsargų kiekis, išdavimo kainos apskaičiavimo metu atsargų kiekis yra teigiamas.</span><span class="sxs-lookup"><span data-stu-id="3ea67-139">**Note:** Although the issues create negative inventory, inventory is positive when the issue price is calculated.</span></span> <span data-ttu-id="3ea67-140">Todėl naudojama einamoji vidutinė savikaina, o ne pagrindiniame prekės įraše esanti kaina.</span><span class="sxs-lookup"><span data-stu-id="3ea67-140">Therefore, the running average cost price is used instead of the price on the item master.</span></span> <span data-ttu-id="3ea67-141">Šiuo momentu sistema turi atsargų vertės 100,00 USD korespondavimą.</span><span class="sxs-lookup"><span data-stu-id="3ea67-141">At this point, the system has an inventory value offset of USD 100.00.</span></span> <span data-ttu-id="3ea67-142">Nors tas poslinkis susidarė dėl 100 prekių, kai vieno vieneto poslinkis buvo 1,00 USD, atsargose dabar turime tik vieną prekę.</span><span class="sxs-lookup"><span data-stu-id="3ea67-142">Although that offset was built up over 100 pieces, where there was a unit offset of USD 1.00 each, we now have only one piece in inventory.</span></span> <span data-ttu-id="3ea67-143">Todėl šiai vienai prekei priskiriamas 100,00 USD poslinkis.</span><span class="sxs-lookup"><span data-stu-id="3ea67-143">Therefore, the offset of USD 100.00 is allocated to this one piece.</span></span> <span data-ttu-id="3ea67-144">Viso to rezultatas – nustatyta per didelė įvertinta savikaina.</span><span class="sxs-lookup"><span data-stu-id="3ea67-144">The result is the overly inflated estimated cost price.</span></span> 

<span data-ttu-id="3ea67-145">**Pastaba:** Palyginimui, atkreipkite dėmesį, kad, jei scenarijuje 2 ir 3 veiksmai sukeičiami, 200 prekių išduodamos 1,51 USD kaina, o vienos prekės vieneto kaina lieka 1,51 USD.</span><span class="sxs-lookup"><span data-stu-id="3ea67-145">**Note:** For comparison, notice that if steps 2 and 3 are reversed in the scenario, 200 items will be issued at a unit price of USD 1.51, and one piece will remain at a unit price of USD 1.51.</span></span> <span data-ttu-id="3ea67-146">Kadangi šis kainos padidinimo scenarijus gali įvykti, kai įtrauktas neigiamas atsargų kiekis, jo sunku išvengti tolesniais atvejais.</span><span class="sxs-lookup"><span data-stu-id="3ea67-146">Because this pricing amplification scenario can occur when negative inventory is involved, it's difficult to avoid in the following cases:</span></span>

-   <span data-ttu-id="3ea67-147">Turite įvertinti išdavimo kainas pagal turimas atsargas ir kiekį.</span><span class="sxs-lookup"><span data-stu-id="3ea67-147">You must estimate issue prices on the on-hand value and quantity.</span></span>
-   <span data-ttu-id="3ea67-148">Turite pakoreguoti turimų atsargų vertę ir kiekį išdavimuose ir gavimuose.</span><span class="sxs-lookup"><span data-stu-id="3ea67-148">You must adjust the on-hand value and quantity on issues and receipts.</span></span>
-   <span data-ttu-id="3ea67-149">Jūsų verslo modelis leidžia išsiųsti arba nustatyti kainas didesniam prekių kiekiui nei turite.</span><span class="sxs-lookup"><span data-stu-id="3ea67-149">Your business model allows you to send out, or price, more pieces than you have.</span></span>
-   <span data-ttu-id="3ea67-150">Turite priimti visų jums pateiktų kvitų vertes ir kiekius.</span><span class="sxs-lookup"><span data-stu-id="3ea67-150">You must accept any receipt value and quantity that are submitted to you.</span></span>

<span data-ttu-id="3ea67-151">Tačiau, jeigu jūsų verslo modelis leidžia taikyti tolesnę praktiką, ji gali padėti išvengti neigiamų kiekių, dėl kurių tampa įmanomas kainos padidinimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="3ea67-151">However, if your business model allows for the following practices, they can help you avoid the negative quantities that make the pricing amplification scenario possible:</span></span>

-   <span data-ttu-id="3ea67-152">Jei pasirenkate prekės parinktį **Įtraukti faktinę vertę**, puslapyje **Prekių modelių grupės** atžymėkite žymės langelį **Faktinės neigiamos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="3ea67-152">If you select the **Include physical value** option for an item, clear the **Physical negative inventory** check box on the **Item model groups** page.</span></span>
-   <span data-ttu-id="3ea67-153">Jei prekės parinkties **Įtraukti faktinę vertę** *nepasirenkate*, puslapyje **Prekių modelių grupės** atžymėkite parinktį **Finansinės neigiamos atsargos**.</span><span class="sxs-lookup"><span data-stu-id="3ea67-153">If you do *not* select the **Include physical value** option for an item, clear the **Financial negative inventory** option on the **Item model groups** page.</span></span>

<span data-ttu-id="3ea67-154">Taip pat turėkite omenyje, kad didžiausias jūsų faktinio atsargų kiekio poslinkis ribojamas pagal faktinių operacijų skaičių ir skirtumą tarp faktinių ir finansinių kainų.</span><span class="sxs-lookup"><span data-stu-id="3ea67-154">Additionally, consider that the maximum offset in your physical inventory value is limited by the number of physical transactions, and the difference between physical and financial prices.</span></span> <span data-ttu-id="3ea67-155">Jei visos faktinės operacijos finansiškai atnaujinamos, faktinė vertė negali pakilti labai aukštai.</span><span class="sxs-lookup"><span data-stu-id="3ea67-155">Provided that all physical transactions are eventually updated financially, the physical value can't rise to extreme levels.</span></span> <span data-ttu-id="3ea67-156">Galiausiai atminkite, kad padidinimo poveikis pastebimai sumažėja sukauptą poslinkį paskirsčius keliems, o ne vienam, turimų atsargų vienetams.</span><span class="sxs-lookup"><span data-stu-id="3ea67-156">Finally, note that the amplification effect decreases significantly when the accumulated offset is spread out over several on-hand pieces instead of just one.</span></span>



