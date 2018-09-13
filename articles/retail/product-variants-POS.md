---
title: "Atsargų peržvalga elektroniniame kasos aparate (EKA)"
description: "Šioje temoje aprašomos parinktys, kuriomis galima peržiūrėti atsargų informaciją elektroniniame kasos aparate (EKA)."
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: e40c558e03ef230fee6726994bc94979d40493c2
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="ceca7-103">Atsargų peržvalga elektroniniame kasos aparate (EKA)</span><span class="sxs-lookup"><span data-stu-id="ceca7-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ceca7-104">Atsargų peržvalga elektroniniame kasos aparate (EKA) padeda mažmenininkams realiuoju laiku gerinti veiklos efektyvumą ir gauti įžvalgų, sujungus parduotuves, EKA ir tarnybinį biurą.</span><span class="sxs-lookup"><span data-stu-id="ceca7-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="ceca7-105">Ši funkcija leidžia tiksliai realiuoju laiku stebėti produkto atsargas visose parduotuvėse ir platinimo centruose.</span><span class="sxs-lookup"><span data-stu-id="ceca7-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="ceca7-106">Ji taip pat padeda mažmenininkams pasiekti papildomo efektyvumo ir sumažinti išlaidas tobulinant atsargų planavimą realiuoju laiku.</span><span class="sxs-lookup"><span data-stu-id="ceca7-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="ceca7-107">Tikslus visos organizacijos atsargų vaizdas realiuoju laiku parduotuvių atstovams padeda teikti savalaikį aukščiausios kokybės klientų aptarnavimą.</span><span class="sxs-lookup"><span data-stu-id="ceca7-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="ceca7-108">Svarbiausias yra tas momentas, kai klientas yra pasirengęs priimti pirkimo sprendimą.</span><span class="sxs-lookup"><span data-stu-id="ceca7-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="ceca7-109">Parduotuvių kasininkams svarbu po ranka turėti realiuoju laiku matomą atsargų informaciją, kad galėtų tiksliai planuoti produktų pristatymą ir paėmimą.</span><span class="sxs-lookup"><span data-stu-id="ceca7-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="ceca7-110">Galite atidaryti puslapį **Atsargų peržvalga** iš darbo srities **„Retail Modern POS“** arba darbo srities **„Retail Cloud POS“**.</span><span class="sxs-lookup"><span data-stu-id="ceca7-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Atsargų peržvalgos dalis EKA pagrindiniame puslapyje](media/POSHomepage.png)

<span data-ttu-id="ceca7-112">Puslapyje **Atsargų peržvalga** galite skaičių klaviatūra įvesti produkto numerį.</span><span class="sxs-lookup"><span data-stu-id="ceca7-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="ceca7-113">Galite peržiūrėti turimus kiekius įvairiose parduotuvėse ir sandėliuose.</span><span class="sxs-lookup"><span data-stu-id="ceca7-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standartinis atsargų peržvalgos puslapis](media/InventoryLookUp.png)

<span data-ttu-id="ceca7-115">Taip pat rodomi kiekvienos vietos **Rezervuoti** ir **Užsakyti** kiekiai.</span><span class="sxs-lookup"><span data-stu-id="ceca7-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="ceca7-116">**Rezervuotas** – šis kiekis rodo pasirinkto vietos produkto numerio **Faktiškai rezervuotą** kiekį tarnybiniame biure.</span><span class="sxs-lookup"><span data-stu-id="ceca7-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="ceca7-117">**Užsakytas** – šis kiekis rodo pasirinkto vietos produkto numerio **Iš viso užsakytą** kiekį tarnybiniame biure.</span><span class="sxs-lookup"><span data-stu-id="ceca7-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="ceca7-118">Vietos, kurių atsargų likučių informacija rodoma</span><span class="sxs-lookup"><span data-stu-id="ceca7-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="ceca7-119">Vietų sąrašas apima dviejų tipų objektus:</span><span class="sxs-lookup"><span data-stu-id="ceca7-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="ceca7-120">**Mažmenines parduotuves** – sąraše pateikiamos parduotuvės, kurios yra sukonfigūruotos naudojant dabartinės parduotuvės lokatorių grupę mažmeninių pardavimų valdyme.</span><span class="sxs-lookup"><span data-stu-id="ceca7-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span> 
- <span data-ttu-id="ceca7-121">**Platinimo centrus** – „Microsoft Dynamics 365 for Retail“ galima sukonfigūruoti įvairių tipų platinimo centrus (pvz., sandėlius).</span><span class="sxs-lookup"><span data-stu-id="ceca7-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="ceca7-122">Tačiau sąraše rodoma informacija apie atsargų likučius tik **Standartinio** numatytojo tipo platinimo centruose.</span><span class="sxs-lookup"><span data-stu-id="ceca7-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="ceca7-123">EKA nerodoma informacija apie atsargų likučius **Tranzito**, **Sulaikymo** ir **Išsiųstų prekių** tipų sandėliuose.</span><span class="sxs-lookup"><span data-stu-id="ceca7-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="ceca7-124">Puslapyje **Atsargų peržvalga** galite peržiūrėti prieinamų atsargų (ATP) kiekį kiekvienoje parduotuvėj, o taip pat ir dabar turimą kiekį, rezervuotą kiekį ir užsakytą kiekį.</span><span class="sxs-lookup"><span data-stu-id="ceca7-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="ceca7-125">Pasirinkite parduotuvę, kurios ATP informaciją norite peržiūrėti, tada pasirinkite **Rodyti parduotuvės pasiekiamumą**.</span><span class="sxs-lookup"><span data-stu-id="ceca7-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP kiekiai](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="ceca7-127">Dimensijų matricos rodinio atidarymas, kad būtų rodomi visi variantai</span><span class="sxs-lookup"><span data-stu-id="ceca7-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="ceca7-128">Bendrojo produkto puslapyje **Produkto informacija** arba puslapyje **Atsargų peržvalga** pasirinkite **Peržiūrėti visus variantus** iš programos juostos puslapio apačioje.</span><span class="sxs-lookup"><span data-stu-id="ceca7-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="ceca7-129">**Dimensijų matricos** rodinys, skirtas pirminiam paleidimui iš šių puslapių, rodo informaciją apie visų produkto variantų atsargų likučius dabartinėje parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="ceca7-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="ceca7-130">Mygtuką **Peržiūrėti visus variantus** galima naudoti tik tame bendrojo produkto elemente, kuriame yra produkto variantų.</span><span class="sxs-lookup"><span data-stu-id="ceca7-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="ceca7-131">Jo nėra atskiruose produktuose ar rinkiniuose.</span><span class="sxs-lookup"><span data-stu-id="ceca7-131">It isn't available for standalone products or kits.</span></span>

![Mygtukas „Peržiūrėti visus variantus“ puslapyje „Atsargų peržvalga“](media/StandardToMatrix.png)

<span data-ttu-id="ceca7-133">Bendrojo produkto puslapyje **Produkto informacija** arba puslapyje **Atsargų peržvalga** pasirinkite **Peržiūrėti visus variantus** nepasirinkdami vietos, kad patektumėte į rodinį **Dimensijų matrica** ir matytumėte informaciją apie visų produkto variantų atsargų likučius dabartinėje parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="ceca7-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Dimensijų matricos rodinys puslapyje „Atsargų peržvalga“](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="ceca7-135">Ankstesnėje iliustracijoje dimensijos rodomos abėcėlės tvarka, nes pasirinkto produkto dimensijų rodymo tvarka nebuvo sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="ceca7-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="ceca7-136">Rodinyje **Dimensijų matrica** produkto variantų langeliuose apatiniame dešiniajame kampe rodoma turimų atsargų vertė.</span><span class="sxs-lookup"><span data-stu-id="ceca7-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="ceca7-137">Įvairių verčių reikšmė yra paaiškinta toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="ceca7-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="ceca7-138">Turima vertė</span><span class="sxs-lookup"><span data-stu-id="ceca7-138">On-hand value</span></span>                            | <span data-ttu-id="ceca7-139">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ceca7-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="ceca7-140">Skaitinė vertė, didesnė už 0 (nulį)</span><span class="sxs-lookup"><span data-stu-id="ceca7-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="ceca7-141">Variantas išleistas pasirinktoje vietoje, langelyje galite atlikti papildomus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ceca7-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="ceca7-142">(Šie veiksmai bus išsamiau aprašyti vėlesniuose šios temos skyriuose.)</span><span class="sxs-lookup"><span data-stu-id="ceca7-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="ceca7-143">**0** (nulis)</span><span class="sxs-lookup"><span data-stu-id="ceca7-143">**0** (zero)</span></span>                             | <span data-ttu-id="ceca7-144">Variantas išleistas pasirinktoje vietoje, bet pasirinktos vietoje šios prekės nėra.</span><span class="sxs-lookup"><span data-stu-id="ceca7-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="ceca7-145">Tačiau langelyje galite atlikti papildomus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ceca7-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="ceca7-146">(Šie veiksmai bus išsamiau aprašyti vėlesniuose šios temos skyriuose.)</span><span class="sxs-lookup"><span data-stu-id="ceca7-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="ceca7-147">**netaikoma** arba neaktyvus langelis</span><span class="sxs-lookup"><span data-stu-id="ceca7-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="ceca7-148">Variantas nebuvo išleistas pasirinktoje vietoje, papildomų veiksmų langelyje atlikti negalite.</span><span class="sxs-lookup"><span data-stu-id="ceca7-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="ceca7-149">Taip pat galite keisti dimensijų suvestinę pasirinkdami naudoti naują dimensiją.</span><span class="sxs-lookup"><span data-stu-id="ceca7-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span> 

![Suvestinės keitimas](media/ChangePivot.png)

![Suvestinė pakeista](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="ceca7-152">Ankstesnėse iliustracijose pasirinkto produkto dimensijų rodymo tvarka yra pasirinktinė (ne pagal abėcėlę).</span><span class="sxs-lookup"><span data-stu-id="ceca7-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="ceca7-153">Ji paremta dimensijų rodymo tvarka, nustatyta tarnybiniame biure.</span><span class="sxs-lookup"><span data-stu-id="ceca7-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="ceca7-154">Be to, rodinyje **Dimensijų matrica** galima atlikti daugiau veiksmų ir tokiu būdu padėti padidinti parduotuvės atstovo produktyvumą.</span><span class="sxs-lookup"><span data-stu-id="ceca7-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="ceca7-155">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="ceca7-155">Here are some examples:</span></span>

- <span data-ttu-id="ceca7-156">Pakeiskite parduotuvės vietą, kad peržvelgtumėte visų produkto variantų atsargų likučius kitose vietose.</span><span class="sxs-lookup"><span data-stu-id="ceca7-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="ceca7-157">Šios vietos apima kitas parduotuves parduotuvių lokatorių grupėje ir **Standartinio** numatytojo tipo platinimo centrus.</span><span class="sxs-lookup"><span data-stu-id="ceca7-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="ceca7-158">Parduokite individualų produkto variantą klientui, taikydami atsiskaitymą grynaisiais, prekių atsiėmimą parduotuvėje arba prekių siuntimą nurodytu adresu.</span><span class="sxs-lookup"><span data-stu-id="ceca7-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="ceca7-159">Pateikite klientui ATP informaciją apie individualų produkto variantą tam tikroje vietoje.</span><span class="sxs-lookup"><span data-stu-id="ceca7-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Papildomi veiksmai variantų dalyse](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="ceca7-161">Ankstesnėje iliustracijoje dimensijos rodomos abėcėlės tvarka, nes pasirinkto produkto dimensijų rodymo tvarka nebuvo sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="ceca7-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="ceca7-162">Šioje lentelėje pateikiama daugiau informacijos apie galimus papildomus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ceca7-162">The following table provides more information about the additional actions that are available.</span></span>


|        <span data-ttu-id="ceca7-163">Veiksmas</span><span class="sxs-lookup"><span data-stu-id="ceca7-163">Action</span></span>        |                                                                                                                    <span data-ttu-id="ceca7-164">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ceca7-164">Description</span></span>                                                                                                                    |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       <span data-ttu-id="ceca7-165">Parduoti dabar</span><span class="sxs-lookup"><span data-stu-id="ceca7-165">Sell now</span></span>       |                               <span data-ttu-id="ceca7-166">Įtraukite pasirinktą prekės variantą į operaciją ir nukreipkite vartotoją į operacijos ekraną.</span><span class="sxs-lookup"><span data-stu-id="ceca7-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="ceca7-167">(Šis veiksmas nėra galimas, kai pasirinkta vieta yra platinimo centras.)</span><span class="sxs-lookup"><span data-stu-id="ceca7-167">(This action isn't available when the selected location is a distribution center.)</span></span>                               |
|   <span data-ttu-id="ceca7-168">Paimti parduotuvėje</span><span class="sxs-lookup"><span data-stu-id="ceca7-168">Pick up in store</span></span>   |      <span data-ttu-id="ceca7-169">Sukurkite kliento užsakymą, skirtą produkto variantui, kuris bus paimtas iš pasirinktos vietos, ir nukreipkite vartotoją į operacijos ekraną.</span><span class="sxs-lookup"><span data-stu-id="ceca7-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="ceca7-170">(Šis veiksmas nėra galimas, kai pasirinkta vieta yra platinimo centras.)</span><span class="sxs-lookup"><span data-stu-id="ceca7-170">(This action isn't available when the selected location is a distribution center.)</span></span>       |
|     <span data-ttu-id="ceca7-171">Siųsti produktą</span><span class="sxs-lookup"><span data-stu-id="ceca7-171">Ship product</span></span>     |                                                 <span data-ttu-id="ceca7-172">Sukurkite kliento užsakymą, skirtą produkto variantui, kuris bus išsiųstas iš pasirinktos vietos, ir nukreipkite vartotoją į operacijos ekraną.</span><span class="sxs-lookup"><span data-stu-id="ceca7-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span>                                                 |
|     <span data-ttu-id="ceca7-173">Prieinamumas</span><span class="sxs-lookup"><span data-stu-id="ceca7-173">Availability</span></span>     |                                                                             <span data-ttu-id="ceca7-174">Rodykite ATP informaciją apie pasirinktą variantų derinį pasirinktoje vietoje.</span><span class="sxs-lookup"><span data-stu-id="ceca7-174">Show the ATP information for the selected variant combination for the selected location.</span></span>                                                                              |
|  <span data-ttu-id="ceca7-175">Visų vietų rodymas</span><span class="sxs-lookup"><span data-stu-id="ceca7-175">Show all locations</span></span>  | <span data-ttu-id="ceca7-176">Pereikite į standartinį atsargų peržvalgos rodinį ir pažymėkite informaciją apie prekės varianto atsargų likučius visose parduotuvėse parduotuvių lokatorių grupėje, taip pat <strong>Standartinio / Numatytojo</strong> tipo platinimo centruose.</span><span class="sxs-lookup"><span data-stu-id="ceca7-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the <strong>Standard/Default</strong> type.</span></span> |
| <span data-ttu-id="ceca7-177">Peržiūrėti produkto informaciją</span><span class="sxs-lookup"><span data-stu-id="ceca7-177">View product details</span></span> |                                                                         <span data-ttu-id="ceca7-178">Nukreipkite vartotoją į susieto bendrojo produkto puslapį <strong>Produkto informacija</strong>.</span><span class="sxs-lookup"><span data-stu-id="ceca7-178">Redirect the user to the <strong>Product details</strong> page of the associated product master.</span></span>                                                                          |

