---
title: „National Motor Freight Classification“ (NMFC) kodai
description: Šioje temoje aprašoma, kaip dirbti su „National Motor Freight Classification“ (NMFC) kodais programoje „Microsoft Dynamics 365 Supply Chain Management“
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 0307437d3868f7ac34fa16a0913907a046ac14d4
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941887"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a><span data-ttu-id="3e3b8-103">„National Motor Freight Classification“ (NMFC) kodai</span><span class="sxs-lookup"><span data-stu-id="3e3b8-103">National Motor Freight Classification (NMFC) codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e3b8-104">„National Motor Freight Classification“ (NMFC) kodai padeda klasifikuoti prekes, kurias galima siųsti.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-104">National Motor Freight Classification (NMFC) codes help you classify items that can be shipped.</span></span> <span data-ttu-id="3e3b8-105">NMFC kodas yra priskyrimas, naudojamas prekių grupavimui.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-105">The NMFC code is a designation that is used to group commodities.</span></span> <span data-ttu-id="3e3b8-106">Tai leidžia transporto įmonėms įvertinti siuntos prekes klasifikuojant prekes pagal tokias aplinkybes, kaip sunkvežimio krovimas, krovinio pakrovimas, tvarkymą ir nebaigtumą.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-106">It enables transport companies to evaluate goods for shipment by classifying items based on considerations such as truck fit, loading issues, handling issues, and perishability.</span></span> <span data-ttu-id="3e3b8-107">Prekės grupuojami į vieną iš 18 transportavimo klasių naudojant numerių diapazoną nuo 50 iki 500.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-107">Commodities are grouped into one of 18 freight classes by using a range of numbers from 50 to 500.</span></span> <span data-ttu-id="3e3b8-108">Klasė, į kurią sugrupuota prekė, pagrįsta keturiomis transportavimo charakteristikomis: tankumu, krovimo galimybėmis, tvarkymu ir įsipareigojimais.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-108">The class that a commodity is grouped into is based on an evaluation of four transportation characteristics: density, stowability, handling, and liability.</span></span> <span data-ttu-id="3e3b8-109">Kartu šios charakteristikos nustato prekės transportavimo galimybes.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-109">Together, these characteristics establish the commodity's transportability.</span></span>

<span data-ttu-id="3e3b8-110">NMFC kodas susietas su kiekvienu mažesniu nei sunkvežimio krovinio (LTL) siuntos elementu.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-110">An NMFC code is associated with every less than truckload (LTL) shipping item.</span></span> <span data-ttu-id="3e3b8-111">Pvz., nešiojamajam kompiuteriui gali būti priskirtas NMFC, kuris yra 2.5 klasė, o elektros įranga – 65 klasės NMFC.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-111">For example, a laptop might be assigned an NMFC that is classed at 2.5, whereas electrical cords might be assigned an NMFC that is classed at 65.</span></span>

<span data-ttu-id="3e3b8-112">Ši funkcija gali padėti darbuotojams naudoti NMFC kodus, klasifikuojant LTL siuntimo prekes.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-112">This feature can help workers use NMFC codes to classify LTL shipping items.</span></span> <span data-ttu-id="3e3b8-113">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="3e3b8-113">Here are some examples:</span></span>

- <span data-ttu-id="3e3b8-114">Jei jūsų įmonėje važtaraštyje (važtaraštis) pateikiamas transportavimo aprašymas, vežėjas tik šiek tiek žinoti, kas yra transportavimas.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-114">If your company includes a freight description on the bill of lading (BOL), the carrier will have some idea what the freight is.</span></span> <span data-ttu-id="3e3b8-115">Transportavimas yra svarbus klasifikavimas, kadangi daugelis transportavimo įmonių visą verslo modelį pagrįsti savo siuntimo transportavimo tipais.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-115">Freight is an important classification because many transportation companies base their whole business model on the types of freight that they ship.</span></span>
- <span data-ttu-id="3e3b8-116">Ši klasifikacija gali būti svarbi jūsų įmonei, nes ji naudojama nustatant dinio krovinio išlaidas.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-116">This classification might be essential to your company because it's used to determine the cost of a given load.</span></span>
- <span data-ttu-id="3e3b8-117">Jūsų įmonė gali nustatyti LTL logistikos ir transportavimo įmonės pelningumą.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-117">Your company can identify the profitability of an LTL logistics and transportation company.</span></span>

<span data-ttu-id="3e3b8-118">Šioje temoje aprašoma, kaip dirbti su NMFC kodais „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-118">This topic describes how to work with NMFC codes in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3e3b8-119">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="3e3b8-119">Prerequisites</span></span>

<span data-ttu-id="3e3b8-120">Prieš kurdami NMFC kodus, turite nustatyti visas LTL transportavimo klases, kurios turi būti susietos su jomis.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-120">Before you can create NMFC codes, you must set up all the LTL freight classes that must be mapped to them.</span></span> <span data-ttu-id="3e3b8-121">LTL transportavimo klasės nurodo prekių kategorijas, o NMFC kodai yra susiję su konkrečiomis prekėmis kiekvienoje iš 18 transportavimo klasių.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-121">LTL freight classes represent categories of items, whereas NMFC codes are related to specific commodities in each of the 18 freight classes.</span></span> <span data-ttu-id="3e3b8-122">Daugiau informacijos apie tai, kaip dirbti su LTL klasėmis, ieškokite mažiau nei [sunkvežimio krovinio (LTL)](ltl-class.md) klasės.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-122">For more information about how to work with LTL classes, see [Less than truckload (LTL) classes](ltl-class.md).</span></span>

## <a name="create-an-nmfc-code"></a><span data-ttu-id="3e3b8-123">NMFC kodo kūrimas</span><span class="sxs-lookup"><span data-stu-id="3e3b8-123">Create an NMFC code</span></span>

<span data-ttu-id="3e3b8-124">Norėdami sukurti NMFC kodą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-124">To create an NMFC code, follow these steps.</span></span>

1. <span data-ttu-id="3e3b8-125">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-125">Follow one of these steps:</span></span>

    - <span data-ttu-id="3e3b8-126">Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> NMFC kodai**.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-126">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
    - <span data-ttu-id="3e3b8-127">Eikite į **Gabenimo valdymas \> Nustatymai \> Gabenimo standartai \> NMFC kodai**.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-127">Go to **Transportation management \> Setup \> Transportation standards \> NMFC codes**.</span></span>

1. <span data-ttu-id="3e3b8-128">Pasirinkite **Nauja**, kad sukurtumėte NMFC kodą.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-128">Select **New** to create an NMFC code.</span></span> <span data-ttu-id="3e3b8-129">Tada nustatykite toliau nurodytus laukus.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-129">Then set the following fields:</span></span>

    - <span data-ttu-id="3e3b8-130">Lauke **NMFC kodas** įveskite NMFC kodą prekės tipui.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-130">**NMFC code** – Enter the NMFC code for the commodity type.</span></span>
    - <span data-ttu-id="3e3b8-131">**Pavadinimas** – Įveskite pavadinimą NMFC kodui.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-131">**Name** – Enter a name for the NMFC code.</span></span>
    - <span data-ttu-id="3e3b8-132">**LTL klasė** – pasirinkite LTL klasę, susietą su NMFC kodu.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-132">**LTL class** – Select the LTL class that is associated with the NMFC code.</span></span>
    - <span data-ttu-id="3e3b8-133">**Važtaraščio** sandėliavimo vienetas – nustatykite numatytąjį siuntos apdorojimo tipą.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-133">**BOL handling unit** – Define the default handling type for the shipment.</span></span>

## <a name="example-set-up-nmfc-codes"></a><span data-ttu-id="3e3b8-134">Pavyzyds: Nustatykite NMFC kodus</span><span class="sxs-lookup"><span data-stu-id="3e3b8-134">Example: Set up NMFC codes</span></span>

<span data-ttu-id="3e3b8-135">Toliau pateikiamas pavyzdys rodo, kaip nustatyti dvi skirtingas NMFC kodai, kuriuos galima naudoti su skirtingais produktų tipais.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-135">The following example shows how to set up two different NMFC codes that can be used with different products.</span></span>

1. <span data-ttu-id="3e3b8-136">Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> NMFC kodai**.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-136">Go to **Warehouse management \> Setup \> Inventory \> NMFC codes**.</span></span>
1. <span data-ttu-id="3e3b8-137">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-137">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3e3b8-138">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="3e3b8-138">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3e3b8-139">**NMFC kodas:** *92.5*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-139">**NMFC code:** *92.5*</span></span>
    - <span data-ttu-id="3e3b8-140">**Pavadinimas:** *Kompiuteriai*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-140">**Name:** *Computers*</span></span>
    - <span data-ttu-id="3e3b8-141">**LTL klasė:** *92,5*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-141">**LTL class:** *92.5*</span></span>
    - <span data-ttu-id="3e3b8-142">**BOL sandėliavimo vienetas:** *vienetas*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-142">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="3e3b8-143">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-143">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="3e3b8-144">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-144">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="3e3b8-145">Naujoje eilutėje nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="3e3b8-145">On the new line, set the following values:</span></span>

    - <span data-ttu-id="3e3b8-146">**NMFC kodas:** *125*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-146">**NMFC code:** *125*</span></span>
    - <span data-ttu-id="3e3b8-147">**Pavadinimas:** *telefonai*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-147">**Name:** *Phones*</span></span>
    - <span data-ttu-id="3e3b8-148">**LTL klasė:** *125*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-148">**LTL class:** *125*</span></span>
    - <span data-ttu-id="3e3b8-149">**BOL sandėliavimo vienetas:** *vienetas*</span><span class="sxs-lookup"><span data-stu-id="3e3b8-149">**BOL handling unit:** *Unit*</span></span>

1. <span data-ttu-id="3e3b8-150">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3e3b8-150">On the Action Pane, select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e3b8-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3e3b8-151">Additional resources</span></span>

- [<span data-ttu-id="3e3b8-152">Mažiau nei sunkvežimio (LTL) krovinių klasės</span><span class="sxs-lookup"><span data-stu-id="3e3b8-152">Less than truckload (LTL) classes</span></span>](ltl-class.md)
- [<span data-ttu-id="3e3b8-153">Važtaraščio kūrimas</span><span class="sxs-lookup"><span data-stu-id="3e3b8-153">Create a bill of landing</span></span>](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
