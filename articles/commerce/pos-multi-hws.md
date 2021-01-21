---
title: Paskirtieji mokėjimo terminalai ir raginimai spausdintuvui ir kasos stalčiui
description: Šioje temoje pateikiama informacija apie galimybę turėti specialų mokėjimo terminalą ir raginti vartotoją pasirinkti kasos stalčių bei kvitų spausdintuvą.
author: rubendel
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 03cb68ede82668523e6970d33df676738e65fd83
ms.sourcegitcommit: 18c5ef10e311f3dd2dbf45c6439ae6beff921af8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2020
ms.locfileid: "3719219"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a><span data-ttu-id="88b9e-103">Paskirtieji mokėjimo terminalai ir raginimai spausdintuvui ir kasos stalčiui</span><span class="sxs-lookup"><span data-stu-id="88b9e-103">Dedicated payment terminals and prompts for a printer and cash drawer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="88b9e-104">Šioje temoje pateikiama informacija apie galimybę turėti specialų mokėjimo terminalą ir raginti vartotoją pasirinkti kasos stalčių bei kvitų spausdintuvą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-104">This topic provides information about the capability to have a dedicated payment terminal and prompt the user to select a cash drawer and a receipt printer.</span></span>

## <a name="overview"></a><span data-ttu-id="88b9e-105">Apžvalga</span><span class="sxs-lookup"><span data-stu-id="88b9e-105">Overview</span></span>

<span data-ttu-id="88b9e-106">Šiuolaikiniai mažmenininkai ieško būdų, kaip supaprastinti atsiskaitymo parduotuvėje patirtį.</span><span class="sxs-lookup"><span data-stu-id="88b9e-106">Modern retailers are searching for ways to streamline the in-store checkout experience.</span></span> <span data-ttu-id="88b9e-107">Naujausios tendencijos kompiuterizuoti atsiskaitymo procesą, naudojant elektroninius mokėjimus, padeda ne tik suteikti pirkimo patirčiai sklandumo, bet ir sumažinti būtinybę turėti visą periferinių įrenginių rinkinį kiekvienam parduotuvės darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="88b9e-107">Recent trends toward paperless checkout through electronic payments not only help to make the purchasing experience smoother but also reduce the need to have a full complement of peripheral devices available for every store associate.</span></span>

<span data-ttu-id="88b9e-108">„Microsoft Dynamics 365 Commerce“ palaiko šias tendencijas, įgalindama scenarijų, kuriame elektroninio kasos aparato (EKA) įrenginys turi jam nuolat paskirtą mokėjimo terminalą, bet jis neprivalo turėti savo kvitų spausdintuvo ar kasos stalčiaus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-108">Microsoft Dynamics 365 Commerce supports these trends by enabling a scenario where a point of sale (POS) device has a dedicated payment terminal assigned to it all the time, but it doesn't have its own receipt printer or cash drawer.</span></span> <span data-ttu-id="88b9e-109">Kai darbuotojams reikia atspausdinti kvitą arba priimti grynuosius pinigus, jie paraginami pasirinkti aparatūros stotį, kurioje sukonfigūruoti šie įrenginiai.</span><span class="sxs-lookup"><span data-stu-id="88b9e-109">When associates must print a receipt or take a cash payment, they are prompted to select a hardware station where those devices are configured.</span></span>

## <a name="key-terms"></a><span data-ttu-id="88b9e-110">Pagrindiniai terminai</span><span class="sxs-lookup"><span data-stu-id="88b9e-110">Key terms</span></span>

| <span data-ttu-id="88b9e-111">Terminas</span><span class="sxs-lookup"><span data-stu-id="88b9e-111">Term</span></span> | <span data-ttu-id="88b9e-112">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="88b9e-112">Description</span></span> |
|---|---|
| <span data-ttu-id="88b9e-113">Registras</span><span class="sxs-lookup"><span data-stu-id="88b9e-113">Register</span></span> | <span data-ttu-id="88b9e-114">Objektas, naudojamas EKA kasos egzemplioriui konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="88b9e-114">The entity that is used to configure an instance of a POS register.</span></span> |
| <span data-ttu-id="88b9e-115">Įrenginys</span><span class="sxs-lookup"><span data-stu-id="88b9e-115">Device</span></span> | <span data-ttu-id="88b9e-116">Fizinio EKA kasoso aparato ir „Modern POS“ programos, kuriai jis priskirtas, egzemplioriaus atvaizdas.</span><span class="sxs-lookup"><span data-stu-id="88b9e-116">A representation of the physical instance of a POS register and the Modern POS application that is assigned to it.</span></span> |
| <span data-ttu-id="88b9e-117">Paskirta aparatūros stotis</span><span class="sxs-lookup"><span data-stu-id="88b9e-117">Dedicated hardware station</span></span> | <span data-ttu-id="88b9e-118">Aparatūros stoties verslo logika yra įtaisyta „Windows“ skirtoje „Modern POS“ ir „Android“ skirtoje „Modern POS“ programose.</span><span class="sxs-lookup"><span data-stu-id="88b9e-118">The hardware station business logic that is built into the Modern POS for Windows and Modern POS for Android applications.</span></span> |
| <span data-ttu-id="88b9e-119">Stalčiaus „Kick“ (d/k) prievadas</span><span class="sxs-lookup"><span data-stu-id="88b9e-119">Drawer kick (d/k) port</span></span> | <span data-ttu-id="88b9e-120">Tradicinis kasos stalčiaus prijungimo prie kvitų spausdintuvo būdas.</span><span class="sxs-lookup"><span data-stu-id="88b9e-120">A traditional method for connecting a cash drawer to a receipt printer.</span></span> |
| <span data-ttu-id="88b9e-121">Išoriniai tinklo įrenginiai</span><span class="sxs-lookup"><span data-stu-id="88b9e-121">Network peripherals</span></span> | <span data-ttu-id="88b9e-122">Integruotas tinklo mokėjimo terminalų, kvitų spausdintuvų ir grynųjų pinigų stalčių palaikymas.</span><span class="sxs-lookup"><span data-stu-id="88b9e-122">Built-in support for network-enabled payment terminals, receipt printers, and cash drawers.</span></span> |

## <a name="supported-pos-clients-and-devices"></a><span data-ttu-id="88b9e-123">Palaikomi EKA klientai ir įrenginiai</span><span class="sxs-lookup"><span data-stu-id="88b9e-123">Supported POS clients and devices</span></span>

<span data-ttu-id="88b9e-124">Šioje temoje aprašytą funkciją palaiko „Modern POS“, skirta „Windows“, ir „Modern POS“, skirta „Android“ EKA klientams.</span><span class="sxs-lookup"><span data-stu-id="88b9e-124">The functionality that is described in this topic is supported by the Modern POS for Windows and Modern POS for Android POS clients.</span></span>

<span data-ttu-id="88b9e-125">Ši funkcija palaiko prie tinklo prijungtus mokėjimo terminalus ir kvitų spausdintuvus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-125">This functionality supports network-enabled payment terminals and receipt printers.</span></span> <span data-ttu-id="88b9e-126">Galite suteikti kasos stalčiaus palaikymą, prijungdami kasos stalčių prie tinklo prijungto kvitų spausdintuvo per d/k prievadą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-126">You can provide cash drawer support by connecting the cash drawer to the network-enabled receipt printer via the d/k port.</span></span>

<span data-ttu-id="88b9e-127">Sąrankos nereikalaujantį šios funkcijos palaikymą teikia [„Dynamics 365 Payment Connector for Adyen“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).</span><span class="sxs-lookup"><span data-stu-id="88b9e-127">Out-of-box support for this functionality is provided by the [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).</span></span> <span data-ttu-id="88b9e-128">Tačiau kitos mokėjimų jungtys gali būti palaikomos naudojant „Commerce Software Development Kit“ (SDK) mokėjimams.</span><span class="sxs-lookup"><span data-stu-id="88b9e-128">However, other payment connectors might be supported via the Commerce software development kit (SDK) for payments.</span></span> <span data-ttu-id="88b9e-129">Palaikomus kvitų spausdintuvus sudaro prie tinklo prijungti „Star Micronics“ ir „Epson“ kvitų spausdintuvai.</span><span class="sxs-lookup"><span data-stu-id="88b9e-129">Supported receipt printers include network-enabled receipt printers from Star Micronics and Epson.</span></span>

<span data-ttu-id="88b9e-130">Norėdami nustatyti „Star Micronics“ kvitų spausdintuvus, naudokite „Star Micronics Printer Utility“, kad sukonfigūruotumėte įrenginį taip, kad jį būtų galima naudoti tinkle.</span><span class="sxs-lookup"><span data-stu-id="88b9e-130">To set up Star Micronics receipt printers, use the Star Micronics Printer Utility to configure the device so that it can be used over the network.</span></span> <span data-ttu-id="88b9e-131">Ši programa taip pat suteiks įrenginiui IP adresą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-131">This utility will also provide the IP address of the device.</span></span>

<span data-ttu-id="88b9e-132">Norėdami nustatyti „Epson“ kvitų spausdintuvus, naudokite „Epson ePOS-Print“ programą, kad sukonfigūruotumėte įrenginį naudoti tinklo protokolus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-132">To set up Epson receipt printers, use the Epson ePOS-Print utility to set up the device to use network protocols.</span></span>

<span data-ttu-id="88b9e-133">Daugiau informacijos apie tai, kaip nustatyti tinklo periferinius įrenginius, žr [Tinklo periferinių įrenginių palaikymo apžvalga](https://go.microsoft.com/fwlink/?linkid=2129965).</span><span class="sxs-lookup"><span data-stu-id="88b9e-133">For more information about how to set up network peripherals, see [Network peripheral support overview](https://go.microsoft.com/fwlink/?linkid=2129965).</span></span>

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a><span data-ttu-id="88b9e-134">Paskirtojo mokėjimų terminalo ir raginimo spausdintuvui bei grynųjų pinigų stalčiui nustatymas</span><span class="sxs-lookup"><span data-stu-id="88b9e-134">Set up a dedicated payment terminal and a prompt for a printer and cash drawer</span></span>

### <a name="set-up-hardware-profiles"></a><span data-ttu-id="88b9e-135">Aparatūros šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="88b9e-135">Set up hardware profiles</span></span>

<span data-ttu-id="88b9e-136">Turite turėti du aparatūros profilio tipus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-136">You must have two types of hardware profile.</span></span> <span data-ttu-id="88b9e-137">Pirmasis priskirta kasos aparatui.</span><span class="sxs-lookup"><span data-stu-id="88b9e-137">The first is assigned to the register.</span></span> <span data-ttu-id="88b9e-138">Antrasis priskirtas aparatūros stočiai parduotuvės lygmenyje ir naudojamas logiškai grupuoti tinklo kvitų spausdintuvams ir grynųjų pinigų stalčiams.</span><span class="sxs-lookup"><span data-stu-id="88b9e-138">The second is assigned to a hardware station at the store level, and is used to logically group network receipt printers and cash drawers.</span></span>

#### <a name="set-up-a-hardware-profile-for-the-register"></a><span data-ttu-id="88b9e-139">Kasos aparato aparatūros profilio nustatymas</span><span class="sxs-lookup"><span data-stu-id="88b9e-139">Set up a hardware profile for the register</span></span>

<span data-ttu-id="88b9e-140">Norėdami nustatyti kasos aparatui priskirtą aparatūros profilį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-140">To set up the hardware profile that is assigned to the register, follow these steps.</span></span>

1. <span data-ttu-id="88b9e-141">Dalyje „Dynamics 365 Commerce“ susiraskite **Aparatūros profilis**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-141">In Dynamics 365 Commerce, search for **Hardware profile**.</span></span>
2. <span data-ttu-id="88b9e-142">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-142">Select **New**.</span></span>
3. <span data-ttu-id="88b9e-143">Priskirkite aparatūros profilio numerį ir įveskite aprašymą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-143">Assign a hardware profile number, and then enter a description.</span></span> <span data-ttu-id="88b9e-144">Šis aparatūros profilis bus priskirtas pačiam kasos aparatui.</span><span class="sxs-lookup"><span data-stu-id="88b9e-144">This hardware profile will be assigned to the register itself.</span></span> <span data-ttu-id="88b9e-145">Todėl, pakaks tokio aprašo, kaip **Paskirtasis su atsarga**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-145">Therefore, a description such as **Dedicated with fallback** will suffice.</span></span>
4. <span data-ttu-id="88b9e-146">Įvairių įrenginių tipų „FastTab“ skirtukuose nustatykite tolesnius įrenginių tipus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-146">On the FastTabs for different device types, set up the following device types.</span></span>

    | <span data-ttu-id="88b9e-147">Įrenginys</span><span class="sxs-lookup"><span data-stu-id="88b9e-147">Device</span></span> | <span data-ttu-id="88b9e-148">Tipas</span><span class="sxs-lookup"><span data-stu-id="88b9e-148">Type</span></span> | <span data-ttu-id="88b9e-149">Įrenginio pavadinimas</span><span class="sxs-lookup"><span data-stu-id="88b9e-149">Device name</span></span> | <span data-ttu-id="88b9e-150">Papildoma informacija</span><span class="sxs-lookup"><span data-stu-id="88b9e-150">Additional details</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="88b9e-151">Spausdintuvas</span><span class="sxs-lookup"><span data-stu-id="88b9e-151">Printer</span></span> | <span data-ttu-id="88b9e-152">Atsarginis</span><span class="sxs-lookup"><span data-stu-id="88b9e-152">Fallback</span></span> | <span data-ttu-id="88b9e-153">*Bet kuris*</span><span class="sxs-lookup"><span data-stu-id="88b9e-153">*Any*</span></span> | <span data-ttu-id="88b9e-154">Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės.</span><span class="sxs-lookup"><span data-stu-id="88b9e-154">The device name is case-sensitive.</span></span> <span data-ttu-id="88b9e-155">**Kvitų profilio ID** turi būti toks pat, kaip **Kvitų profilio ID**, kuris yra susietas su tinklo spausdintuvu, kuris yra susietas su aparatūros profiliu, priskirtu aparatūros stočiai kanalo lygmeniu.</span><span class="sxs-lookup"><span data-stu-id="88b9e-155">The **Receipt profile ID** should be the same as the **Receipt profile ID** that is mapped to the network printer that is set up in the hardware profile that is assigned to the hardware station at the channel level.</span></span> |
    | <span data-ttu-id="88b9e-156">Kasos stalčius</span><span class="sxs-lookup"><span data-stu-id="88b9e-156">Cash drawer</span></span> | <span data-ttu-id="88b9e-157">Atsarginis</span><span class="sxs-lookup"><span data-stu-id="88b9e-157">Fallback</span></span> | <span data-ttu-id="88b9e-158">*Bet kuris*</span><span class="sxs-lookup"><span data-stu-id="88b9e-158">*Any*</span></span> | <span data-ttu-id="88b9e-159">Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės.</span><span class="sxs-lookup"><span data-stu-id="88b9e-159">The device name is case-sensitive.</span></span> <span data-ttu-id="88b9e-160">Nustatykite parinktį **Naudoti bendrą pamainą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-160">Set the **Use shared shift** option to **Yes**.</span></span> |
    | <span data-ttu-id="88b9e-161">EFT paslauga</span><span class="sxs-lookup"><span data-stu-id="88b9e-161">EFT service</span></span> | <span data-ttu-id="88b9e-162">„Adyen“</span><span class="sxs-lookup"><span data-stu-id="88b9e-162">Adyen</span></span> | <span data-ttu-id="88b9e-163">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="88b9e-163">Not applicable</span></span> | <span data-ttu-id="88b9e-164">Informacijos apie tai, kaip nustatyti naują „Adyen“ jungtį, žr. [„Dynamics 365 Payment Connector for Adyen“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).</span><span class="sxs-lookup"><span data-stu-id="88b9e-164">For information about how to set up the out-of-box Adyen connector, see [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).</span></span> <span data-ttu-id="88b9e-165">Kitos mokėjimų jungtys gali būti palaikomos naudojant [„Commerce Software Development Kit“ (SDK) mokėjimams](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension).</span><span class="sxs-lookup"><span data-stu-id="88b9e-165">Other payment connectors can be supported via the [Commerce software development kit (SDK) for payments](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension).</span></span> |
    | <span data-ttu-id="88b9e-166">PIN rinkiklis</span><span class="sxs-lookup"><span data-stu-id="88b9e-166">PIN pad</span></span> | <span data-ttu-id="88b9e-167">Tinklas</span><span class="sxs-lookup"><span data-stu-id="88b9e-167">Network</span></span> | <span data-ttu-id="88b9e-168">**MicrosoftAdyenDeviceV001**</span><span class="sxs-lookup"><span data-stu-id="88b9e-168">**MicrosoftAdyenDeviceV001**</span></span> | <span data-ttu-id="88b9e-169">Nėra.</span><span class="sxs-lookup"><span data-stu-id="88b9e-169">None.</span></span> |

5. <span data-ttu-id="88b9e-170">Programoje „Dynamics 365 Commerce“ susiraskite **Kasos aparatai**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-170">In Dynamics 365 Commerce, search for **Registers**.</span></span>
6. <span data-ttu-id="88b9e-171">Pasirinkite kasos aparatą pasirinkdami kasos aparato numerį ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-171">Select a register by selecting the register number, and then select **Edit**.</span></span>
7. <span data-ttu-id="88b9e-172">Priskirkite ką tik sukurtą aparatūros profilį kasos aparate, kuris turėtų naudoti paskirtąjį mokėjimo terminalą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-172">Assign the hardware profile that you just created to the register that should use a dedicated payment terminal.</span></span> <span data-ttu-id="88b9e-173">Įrenginys, susietas su šiuo kasos aparatu, turi naudoti programą „Modern POS“, skirtą Windows, arba „Modern POS“, skirtą „Android“.</span><span class="sxs-lookup"><span data-stu-id="88b9e-173">The device that is mapped to this register must use either the Modern POS for Windows application or the Modern POS for Android application.</span></span>
8. <span data-ttu-id="88b9e-174">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-174">Select **Save**.</span></span>
9. <span data-ttu-id="88b9e-175">Veiksmų srities skirtuke **Kasos aparatai** pasirinkite **Konfigūruoti IP adresus**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-175">On the Action Pane, on the **Registers** tab, select **Configure IP addresses**.</span></span>
10. <span data-ttu-id="88b9e-176">„FastTab“ skirtuke **PIN rinkiklis** įveskite mokėjimo terminalo IP adresą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-176">On the **PIN pad** FastTab, enter the IP address of the payment terminal.</span></span> <span data-ttu-id="88b9e-177">Daugiau informacijos apie tai, kaip gauti mokėjimo terminalo IP adresą naudojant „Adyen“ jungtį, žr [„Dynamics 365 Payment Connector for Adyen“](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).</span><span class="sxs-lookup"><span data-stu-id="88b9e-177">For information about how to get the IP address of the payment terminal by using the Adyen connector, see [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).</span></span>
11. <span data-ttu-id="88b9e-178">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-178">Select **Save**.</span></span>

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a><span data-ttu-id="88b9e-179">Aparatūros profilio nustatymas kvitų spausdintuvui ir grynųjų pinigų stalčiui</span><span class="sxs-lookup"><span data-stu-id="88b9e-179">Set up a hardware profile for the receipt printer and cash drawer</span></span>

<span data-ttu-id="88b9e-180">Norėdami nustatyti aparatūros profilį, naudojamą tinklo kvitų spausdintuvui ir grynųjų pinigų stalčiui sugrupuoti, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-180">To set up the hardware profile that is used to group the network receipt printer and cash drawer, follow these steps.</span></span>

1. <span data-ttu-id="88b9e-181">Dalyje „Dynamics 365 Commerce“ susiraskite **Aparatūros profilis**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-181">In Dynamics 365 Commerce, search for **Hardware profile**.</span></span>
2. <span data-ttu-id="88b9e-182">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-182">Select **New**.</span></span>
3. <span data-ttu-id="88b9e-183">Priskirkite aparatūros profilio numerį ir įveskite aprašymą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-183">Assign a hardware profile number, and then enter a description.</span></span> <span data-ttu-id="88b9e-184">Šis aparatūros profilis bus naudojamas kvitų spausdintuvui ir grynųjų pinigų stalčiui sugrupuoti.</span><span class="sxs-lookup"><span data-stu-id="88b9e-184">This hardware profile will be used to group the receipt printer and cash drawer.</span></span> <span data-ttu-id="88b9e-185">Todėl pakaks tokio aprašymo, kaip **Tinklo spausdintuvas ir grynųjų pinigų stalčius**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-185">Therefore, a description such as **Network printer and cash drawer** will suffice.</span></span>
4. <span data-ttu-id="88b9e-186">Įvairių įrenginių tipų „FastTab“ skirtukuose nustatykite tolesnius įrenginių tipus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-186">On the FastTabs for different device types, set up the following device types.</span></span>

    | <span data-ttu-id="88b9e-187">Įrenginys</span><span class="sxs-lookup"><span data-stu-id="88b9e-187">Device</span></span> | <span data-ttu-id="88b9e-188">Tipas</span><span class="sxs-lookup"><span data-stu-id="88b9e-188">Type</span></span> | <span data-ttu-id="88b9e-189">aprašymas</span><span class="sxs-lookup"><span data-stu-id="88b9e-189">Description</span></span> | <span data-ttu-id="88b9e-190">Papildoma informacija</span><span class="sxs-lookup"><span data-stu-id="88b9e-190">Additional details</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="88b9e-191">Spausdintuvas</span><span class="sxs-lookup"><span data-stu-id="88b9e-191">Printer</span></span> | <span data-ttu-id="88b9e-192">Tinklas</span><span class="sxs-lookup"><span data-stu-id="88b9e-192">Network</span></span> | <span data-ttu-id="88b9e-193">**„Epson“** arba **„Star“**</span><span class="sxs-lookup"><span data-stu-id="88b9e-193">**Epson** or **Star**</span></span> | <span data-ttu-id="88b9e-194">Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės.</span><span class="sxs-lookup"><span data-stu-id="88b9e-194">The device name is case-sensitive.</span></span> <span data-ttu-id="88b9e-195">**Kvitų profilio ID** turi būti toks pat, kaip **Kvitų profilio ID**, kuris yra susietas su spausdintuvu, kuris yra susietas su aparatūros profiliu, priskirtu kasos aparatui.</span><span class="sxs-lookup"><span data-stu-id="88b9e-195">The **Receipt profile ID** should be the same as the **Receipt profile ID** that is mapped to the printer that is set up in the hardware profile that is assigned to the register.</span></span> |
    | <span data-ttu-id="88b9e-196">Kasos stalčius</span><span class="sxs-lookup"><span data-stu-id="88b9e-196">Cash drawer</span></span> | <span data-ttu-id="88b9e-197">Tinklas</span><span class="sxs-lookup"><span data-stu-id="88b9e-197">Network</span></span> | <span data-ttu-id="88b9e-198">**„Epson“** arba **„Star“**</span><span class="sxs-lookup"><span data-stu-id="88b9e-198">**Epson** or **Star**</span></span> | <span data-ttu-id="88b9e-199">Skiriamos didžiosios ir mažosios įrenginio pavadinimo raidės.</span><span class="sxs-lookup"><span data-stu-id="88b9e-199">The device name is case-sensitive.</span></span> <span data-ttu-id="88b9e-200">Nustatykite parinktį **Naudoti bendrą pamainą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-200">set the **Use shared shift** option to **Yes**.</span></span> |

5. <span data-ttu-id="88b9e-201">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-201">Select **Save**.</span></span>

### <a name="set-up-hardware-stations"></a><span data-ttu-id="88b9e-202">Aparatūros stočių nustatymas</span><span class="sxs-lookup"><span data-stu-id="88b9e-202">Set up hardware stations</span></span>

<span data-ttu-id="88b9e-203">Turite turėti dvi aparatūros stotis.</span><span class="sxs-lookup"><span data-stu-id="88b9e-203">You must have two hardware stations.</span></span> <span data-ttu-id="88b9e-204">Pirmoji bus susieta su kasos aparatu.</span><span class="sxs-lookup"><span data-stu-id="88b9e-204">The first will be mapped to the register.</span></span> <span data-ttu-id="88b9e-205">Antroji bus pasirinkta kaip reikalinga, kai reikia atspausdinti kvitą arba atidaryti grynųjų pinigų stalčių.</span><span class="sxs-lookup"><span data-stu-id="88b9e-205">The second will be selected as it's required, whenever a receipt must be printed or a cash drawer must be opened.</span></span>

#### <a name="register-a-hardware-station"></a><span data-ttu-id="88b9e-206">Kasos aparato aparatūros stotis</span><span class="sxs-lookup"><span data-stu-id="88b9e-206">Register a hardware station</span></span>

1. <span data-ttu-id="88b9e-207">Programoje „Dynamics 365 Commerce“ susiraskite **Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-207">In Dynamics 365 Commerce, search for **All stores**.</span></span>
2. <span data-ttu-id="88b9e-208">Pasirinkite parduotuvę pasirinkdami jos **Mažmeninės prekybos kanalo ID** reikšmes ir pasirinkdami **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-208">Select a store by selecting its **Retail Channel Id** values, and then select **Edit**.</span></span>
3. <span data-ttu-id="88b9e-209">„FastTab“ skirtuke **Aparatūros stotys** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-209">On the **Hardware stations** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="88b9e-210">Nustatykite **Aparatūros stoties tipo** lauką į **Paskirtasis**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-210">Set the **Hardware station type** field to **Dedicated**.</span></span>
5. <span data-ttu-id="88b9e-211">Įveskite aprašymą, bet nenustatykite jokių kitų šios aparatūros stoties verčių.</span><span class="sxs-lookup"><span data-stu-id="88b9e-211">Enter a description, but don't set any other values for this hardware station.</span></span> <span data-ttu-id="88b9e-212">Ši aparatūros stotis bus naudojama kasos aparatui visą laiką.</span><span class="sxs-lookup"><span data-stu-id="88b9e-212">This hardware station will be used for the register at all times.</span></span> 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a><span data-ttu-id="88b9e-213">Aparatūros stoties nustatymas kvitų spausdintuvui ir grynųjų pinigų stalčiui</span><span class="sxs-lookup"><span data-stu-id="88b9e-213">Set up a hardware station for the receipt printer and cash drawer</span></span>

1. <span data-ttu-id="88b9e-214">Programoje „Dynamics 365 Commerce“ susiraskite **Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-214">In Dynamics 365 Commerce, search for **All stores**.</span></span>
2. <span data-ttu-id="88b9e-215">Pasirinkite parduotuvę pasirinkdami jos **Mažmeninės prekybos kanalo ID** reikšmes ir pasirinkdami **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-215">Select a store by selecting its **Retail Channel Id** values, and then select **Edit**.</span></span>
3. <span data-ttu-id="88b9e-216">„FastTab“ skirtuke **Aparatūros stotys** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-216">On the **Hardware stations** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="88b9e-217">Nustatykite **Aparatūros stoties tipo** lauką į **Paskirtasis**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-217">Set the **Hardware station type** field to **Dedicated**.</span></span>
5. <span data-ttu-id="88b9e-218">Įvesti aprašymą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-218">Enter a description.</span></span> <span data-ttu-id="88b9e-219">Ši aparatūros stotis bus naudojama kvitų spausdintuvui ir grynųjų pinigų stalčiui.</span><span class="sxs-lookup"><span data-stu-id="88b9e-219">This hardware station will be used for the receipt printer and cash drawer.</span></span>
6. <span data-ttu-id="88b9e-220">Lauke **Aparatūros profilis**pasirinkite aparatūros profilį, kurį anksčiau sukūrėte kvitų spausdintuvui ir grynųjų pinigų stalčiui.</span><span class="sxs-lookup"><span data-stu-id="88b9e-220">In the **Hardware profile** field, select the hardware profile that you previously created for the receipt printer and cash drawer.</span></span>
7. <span data-ttu-id="88b9e-221">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-221">Select **Save**.</span></span>
8. <span data-ttu-id="88b9e-222">Kol aparatūros stotis kvitų spausdintuvui ir grynųjų pinigų vis dar renkama, pasirinkite **Konfigūruoti IP adresus**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-222">While the hardware station for the receipt printer and cash drawer is still selected, select **Configure IP addresses**.</span></span>
9. <span data-ttu-id="88b9e-223">Sužinokite spausdintuvo IP adresą ir įveskite jį kaip IP adresą, skirtą kvitų spausdintuvui ir grynųjų pinigų stalčiui.</span><span class="sxs-lookup"><span data-stu-id="88b9e-223">Obtain the IP address for the printer, and enter it as the IP address for both the receipt printer and the cash drawer.</span></span>
10. <span data-ttu-id="88b9e-224">Pasirinkite **Įrašyti**</span><span class="sxs-lookup"><span data-stu-id="88b9e-224">Select **Save**</span></span>
11. <span data-ttu-id="88b9e-225">Susiraskite **Paskirstymo grafikai**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-225">Search for **Distribution schedules**.</span></span>
12. <span data-ttu-id="88b9e-226">Pasirinkite paskirstymo grafiką **1090**, tada pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-226">Select distribution schedule **1090**, and then select **Run now**.</span></span>
13. <span data-ttu-id="88b9e-227">Pasirinkite paskirstymo grafiką **1070**, tada pasirinkite **Vykdyti dabar**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-227">Select distribution schedule **1070**, and then select **Run now**.</span></span>

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a><span data-ttu-id="88b9e-228">Nustatymas, kad sistema ragintų pasirinkti kvitų spausdintuvą ir grynųjų pinigų stalčių, kai jo prireikia</span><span class="sxs-lookup"><span data-stu-id="88b9e-228">Set up the system to prompt for receipt printer and cash drawer selection as it's required</span></span>

1. <span data-ttu-id="88b9e-229">Palaikomame EKA kliente uždarykite dabartinę pamainą, jei pamaina atidaryta.</span><span class="sxs-lookup"><span data-stu-id="88b9e-229">In a supported POS client, close the current shift, if a shift is open.</span></span>
2. <span data-ttu-id="88b9e-230">Prisijunkite ir pasirinkite **Stalčiaus operacijos be stalčiaus**.</span><span class="sxs-lookup"><span data-stu-id="88b9e-230">Sign in, and then select **Non-drawer drawer operations**.</span></span>
3. <span data-ttu-id="88b9e-231">Naudokite operaciją **Valdyti aparatūros stotis**, kad aparatūros stočiai įjungti.</span><span class="sxs-lookup"><span data-stu-id="88b9e-231">Use the **Manage hardware stations** operation to turn on a hardware station.</span></span>
4. <span data-ttu-id="88b9e-232">Pasirinkite aparatūros stotį, kurią sukūrėte kasos aparatui, kad taptų aktyvi.</span><span class="sxs-lookup"><span data-stu-id="88b9e-232">Select the hardware station that you created for the register to make it active.</span></span>
5. <span data-ttu-id="88b9e-233">Atsijunkite nuo EKA, vėl prisijunkite ir atidarykite pamainą.</span><span class="sxs-lookup"><span data-stu-id="88b9e-233">Sign out of the POS, sign back in, and open a shift.</span></span>

<span data-ttu-id="88b9e-234">Mokėjimo terminalas, kuris priskirtas aparatūros profiliui, nuo šiol visada bus aktyvus, o jūs būsite raginami, jei prireiktų kvitų spausdintuvo arba kasos stalčiaus.</span><span class="sxs-lookup"><span data-stu-id="88b9e-234">The payment terminal that is assigned to the hardware profile will now always be active, and you will be prompted if a receipt printer or cash drawer is required.</span></span>

<span data-ttu-id="88b9e-235">Daugelis pardavėjų, kurie prašė šios funkcijos, siekia mažinti atliekų kiekį, siųsdami kvitus el. paštu ir ragindami atsiskaityti elektroniniu būdu.</span><span class="sxs-lookup"><span data-stu-id="88b9e-235">Many merchants who requested this feature are interested in reducing waste by providing email receipts and encouraging electronic payments.</span></span> <span data-ttu-id="88b9e-236">Priklausomai nuo EKA konfigūracijos, parduotuvių darbuotojai raginami pasirinkti kvitų spausdintuvą arba grynųjų pinigų stalčių tik tada, kai klientas nori gauti fizinį kvitą arba nori atsiskaityti grynaisiais pinigais.</span><span class="sxs-lookup"><span data-stu-id="88b9e-236">Depending on the configuration of the POS, store associates are prompted to select a receipt printer or cash drawer only when a customer wants a physical receipt or wants to pay with cash.</span></span>

<span data-ttu-id="88b9e-237">Parduotuvės darbuotojai raginami pasirinkti aparatūros stotį tik vieną kartą per operaciją, išskyrus atvejus, kai reikia atspausdinti kvitą ir atsikaitoma grynaisiais pinigais, bet anksčiau pasirinktame aparatūros profilyje neįtraukti abu įrenginiai.</span><span class="sxs-lookup"><span data-stu-id="88b9e-237">Store associates are prompted to select a hardware station only one time per transaction, unless a receipt must be printed and cash is used for payment, but the hardware profile that was originally selected doesn't include both devices.</span></span> <span data-ttu-id="88b9e-238">Tokiu atveju parduotuvės darbuotojas bus paragintas dar kartą, kad pasirinktų aparatūros stotį, kurią galima naudoti operacijai atlikti.</span><span class="sxs-lookup"><span data-stu-id="88b9e-238">In that case, the store associate will be prompted again to select a hardware station that can be used to complete the transaction.</span></span>

## <a name="related-articles"></a><span data-ttu-id="88b9e-239">Susiję straipsniai</span><span class="sxs-lookup"><span data-stu-id="88b9e-239">Related articles</span></span>

- [<span data-ttu-id="88b9e-240">Programos „POS Hybrid“ nustatymas sistemose „Android“ ir „iOS“</span><span class="sxs-lookup"><span data-stu-id="88b9e-240">Set up POS hybrid app on Android and iOS</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [<span data-ttu-id="88b9e-241">„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“</span><span class="sxs-lookup"><span data-stu-id="88b9e-241">Dynamics 365 Payment Connector for Adyen</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [<span data-ttu-id="88b9e-242">Tinklo periferinių įrenginių palaikymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="88b9e-242">Network peripheral support overview</span></span>](https://go.microsoft.com/fwlink/?linkid=2129965)