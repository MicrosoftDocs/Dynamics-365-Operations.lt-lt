---
title: Numatytojo kliento kūrimas
description: Šioje temoje aprašoma, kaip sukurti numatytąjį klientą, kuris bus naudojamas kuriant kanalą programoje „Microsoft Dynamics 365 Commerce“.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f988732549ce82919f02c87b320623d8d4218735
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477905"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="c8dd5-103">Numatytojo kliento kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8dd5-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8dd5-104">Šioje temoje aprašoma, kaip sukurti numatytąjį klientą, kuris bus naudojamas kuriant kanalą programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c8dd5-105">Kuriant kanalą, reikės pateikti numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="c8dd5-106">Numatytąjį klientą galima lengvai sukurti, pirma sukūrus klientų grupę ir klientų adresų knygelė.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="c8dd5-107">Klientų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8dd5-107">Create a customer group</span></span>

<span data-ttu-id="c8dd5-108">Jei klientų grupių dar nėra, galite ją sukurti.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="c8dd5-109">Pavyzdžiui, gali būti grupių, apimančių skirtingas klientų grupes, pvz., didmeninė prekyba, mažmeninė prekyba, internetas, darbuotojai ir pan.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="c8dd5-110">Norėdami sukurti klientų grupę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="c8dd5-111">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Klientai \> Klientų grupės**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="c8dd5-112">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8dd5-113">Langelyje **Klientų grupė** įveskite klientų grupės ID.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="c8dd5-114">Langelyje **Aprašas** įveskite tinkamą aprašą.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="c8dd5-115">Langelyje **Mokėjimo sąlygos** įveskite tinkamą vertę.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="c8dd5-116">Langelyje **Laikotarpis nuo SF termino iki mokėjimo datos** įveskite tinkamą vertę.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="c8dd5-117">Langelyje **Numatytoji mokesčių grupė** įveskite mokesčių grupę, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="c8dd5-118">Pažymėkite žymės langelį **Kainos su PVM**, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="c8dd5-119">Langelyje **Numatytojo nurašymo priežastis** įveskite tinkamą vertę, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="c8dd5-120">Toliau pateiktame vaizde parodytos kelios sukonfigūruotos klientų grupės.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-120">The following image shows several configured customer groups.</span></span>

![Klientų grupės](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="c8dd5-122">Klientų adresų knygelės kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8dd5-122">Create a customer address book</span></span>

<span data-ttu-id="c8dd5-123">Klientas turi būti susietas su adresų knygele.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="c8dd5-124">Jeigu adresų knygelė dar nesukurta, reikės ją sukurti.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="c8dd5-125">Norėdami sukurti klientų adresų knygelę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="c8dd5-126">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Adresų knygelės**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="c8dd5-127">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8dd5-128">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="c8dd5-129">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="c8dd5-130">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="c8dd5-131">Toliau pateiktame vaizde parodytas adresų knygelės pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-131">The following image shows an example address book.</span></span>

![Adresų knygelė](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="c8dd5-133">Numatytojo kliento kūrimas</span><span class="sxs-lookup"><span data-stu-id="c8dd5-133">Create a default customer</span></span>

<span data-ttu-id="c8dd5-134">Norėdami sukurti numatytąjį klientą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="c8dd5-135">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Klientai \> Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="c8dd5-136">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="c8dd5-137">Išplečiamajame sąraše **Tipas** pasirinkite „Asmuo“.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="c8dd5-138">Išplečiamajame sąraše **Kliento sąskaita** pasirinkite arba įveskite sąskaitos numerį (pvz., „100001“).</span><span class="sxs-lookup"><span data-stu-id="c8dd5-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="c8dd5-139">Išplečiamajame sąraše **Vardas** pasirinkite arba įveskite vardą (pavyzdžiui, „Numatytasis“).</span><span class="sxs-lookup"><span data-stu-id="c8dd5-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="c8dd5-140">Išplečiamajame sąraše **Antras vardas** pasirinkite arba įveskite vardą (pavyzdžiui, „Mažmeninė prekyba“).</span><span class="sxs-lookup"><span data-stu-id="c8dd5-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="c8dd5-141">Išplečiamajame sąraše **Pavardė** pasirinkite arba įveskite vardą (pavyzdžiui, „Klientas“).</span><span class="sxs-lookup"><span data-stu-id="c8dd5-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="c8dd5-142">Išplečiamajame sąraše **Valiuta** pasirinkite arba įveskite valiutą (pavyzdžiui, „JAV doleris“).</span><span class="sxs-lookup"><span data-stu-id="c8dd5-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="c8dd5-143">Išplečiamajame sąraše **Valiuta** pasirinkite anksčiau sukurtą klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="c8dd5-144">Išplečiamajame sąraše **Adresų knygelės** pasirinkite esamą kliento adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="c8dd5-145">Pasirinkite **Įrašyti**, kad įrašytumėte ir grįžtumėte į naujo kliento informacijos ekraną.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="c8dd5-146">Nebūtina įtraukti numatytojo kliento adreso.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="c8dd5-147">Toliau pateiktame vaizde parodytas kliento kūrimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-147">The following image shows an example of customer creation.</span></span>

![Numatytojo kliento kūrimas](media/default-customer-creation.png)

<span data-ttu-id="c8dd5-149">Toliau pateiktame vaizde parodytas numatytojo kliento konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-149">The following image shows a default customer configuration.</span></span>

![Kliento konfigūravimo pavyzdys](media/default-customer-configuration1.png)

<span data-ttu-id="c8dd5-151">Dauguma numatytųjų verčių kliento informacijos ekrane gali likti, bet dvi vertes reikia pakeisti.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="c8dd5-152">Kliento informacijos ekrane išplėskite **Pardavimo užsakymo numatytieji nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="c8dd5-153">Išplečiamajame sąraše **Svetainė** pasirinkite arba įveskite iš anksto sukonfigūruotą svetainę.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="c8dd5-154">Išplečiamajame sąraše **Sandėlis** pasirinkite arba įveskite iš anksto sukonfigūruotą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="c8dd5-155">Toliau pateiktame vaizde parodytas kliento konfigūravimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c8dd5-155">The following image shows an example customer configuration.</span></span>

![Kliento konfigūravimo pavyzdys](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="c8dd5-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c8dd5-157">Additional resources</span></span>

[<span data-ttu-id="c8dd5-158">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="c8dd5-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c8dd5-159">Kanalo sąrankos būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="c8dd5-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
