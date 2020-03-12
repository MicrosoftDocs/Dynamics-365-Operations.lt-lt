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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ba1d10a897f349703737068d772423f7d0292944
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057967"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="a061d-103">Numatytojo kliento kūrimas</span><span class="sxs-lookup"><span data-stu-id="a061d-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a061d-104">Šioje temoje aprašoma, kaip sukurti numatytąjį klientą, kuris bus naudojamas kuriant kanalą programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="a061d-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a061d-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="a061d-105">Overview</span></span>

<span data-ttu-id="a061d-106">Kuriant kanalą, reikės pateikti numatytąjį klientą.</span><span class="sxs-lookup"><span data-stu-id="a061d-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="a061d-107">Numatytąjį klientą galima lengvai sukurti, pirma sukūrus klientų grupę ir klientų adresų knygelė.</span><span class="sxs-lookup"><span data-stu-id="a061d-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="a061d-108">Klientų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="a061d-108">Create a customer group</span></span>

<span data-ttu-id="a061d-109">Jei klientų grupių dar nėra, galite ją sukurti.</span><span class="sxs-lookup"><span data-stu-id="a061d-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="a061d-110">Pavyzdžiui, gali būti grupių, apimančių skirtingas klientų grupes, pvz., didmeninė prekyba, mažmeninė prekyba, internetas, darbuotojai ir pan.</span><span class="sxs-lookup"><span data-stu-id="a061d-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="a061d-111">Norėdami sukurti klientų grupę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a061d-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="a061d-112">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Klientai \> Klientų grupės**.</span><span class="sxs-lookup"><span data-stu-id="a061d-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="a061d-113">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="a061d-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a061d-114">Langelyje **Klientų grupė** įveskite klientų grupės ID.</span><span class="sxs-lookup"><span data-stu-id="a061d-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="a061d-115">Langelyje **Aprašas** įveskite tinkamą aprašą.</span><span class="sxs-lookup"><span data-stu-id="a061d-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="a061d-116">Langelyje **Mokėjimo sąlygos** įveskite tinkamą vertę.</span><span class="sxs-lookup"><span data-stu-id="a061d-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="a061d-117">Langelyje **Laikotarpis nuo SF termino iki mokėjimo datos** įveskite tinkamą vertę.</span><span class="sxs-lookup"><span data-stu-id="a061d-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="a061d-118">Langelyje **Numatytoji mokesčių grupė** įveskite mokesčių grupę, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="a061d-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="a061d-119">Pažymėkite žymės langelį **Kainos su PVM**, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="a061d-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="a061d-120">Langelyje **Numatytojo nurašymo priežastis** įveskite tinkamą vertę, jei taikoma.</span><span class="sxs-lookup"><span data-stu-id="a061d-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="a061d-121">Toliau pateiktame vaizde parodytos kelios sukonfigūruotos klientų grupės.</span><span class="sxs-lookup"><span data-stu-id="a061d-121">The following image shows several configured customer groups.</span></span>

![Klientų grupės](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="a061d-123">Klientų adresų knygelės kūrimas</span><span class="sxs-lookup"><span data-stu-id="a061d-123">Create a customer address book</span></span>

<span data-ttu-id="a061d-124">Klientas turi būti susietas su adresų knygele.</span><span class="sxs-lookup"><span data-stu-id="a061d-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="a061d-125">Jeigu adresų knygelė dar nesukurta, reikės ją sukurti.</span><span class="sxs-lookup"><span data-stu-id="a061d-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="a061d-126">Norėdami sukurti klientų adresų knygelę, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a061d-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="a061d-127">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Adresų knygelės**.</span><span class="sxs-lookup"><span data-stu-id="a061d-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="a061d-128">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="a061d-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a061d-129">Langelyje **Pavadinimas** įveskite pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="a061d-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="a061d-130">Langelyje **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="a061d-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="a061d-131">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a061d-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a061d-132">Toliau pateiktame vaizde parodytas adresų knygelės pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a061d-132">The following image shows an example address book.</span></span>

![Adresų knygelė](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="a061d-134">Numatytojo kliento kūrimas</span><span class="sxs-lookup"><span data-stu-id="a061d-134">Create a default customer</span></span>

<span data-ttu-id="a061d-135">Norėdami sukurti numatytąjį klientą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a061d-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="a061d-136">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Klientai \> Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="a061d-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="a061d-137">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="a061d-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a061d-138">Išplečiamajame sąraše **Tipas** pasirinkite „Asmuo“.</span><span class="sxs-lookup"><span data-stu-id="a061d-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="a061d-139">Išplečiamajame sąraše **Kliento sąskaita** pasirinkite arba įveskite sąskaitos numerį (pvz., „100001“).</span><span class="sxs-lookup"><span data-stu-id="a061d-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="a061d-140">Išplečiamajame sąraše **Vardas** pasirinkite arba įveskite vardą (pavyzdžiui, „Numatytasis“).</span><span class="sxs-lookup"><span data-stu-id="a061d-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="a061d-141">Išplečiamajame sąraše **Antras vardas** pasirinkite arba įveskite vardą (pavyzdžiui, „Mažmeninė prekyba“).</span><span class="sxs-lookup"><span data-stu-id="a061d-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="a061d-142">Išplečiamajame sąraše **Pavardė** pasirinkite arba įveskite vardą (pavyzdžiui, „Klientas“).</span><span class="sxs-lookup"><span data-stu-id="a061d-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="a061d-143">Išplečiamajame sąraše **Valiuta** pasirinkite arba įveskite valiutą (pavyzdžiui, „JAV doleris“).</span><span class="sxs-lookup"><span data-stu-id="a061d-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="a061d-144">Išplečiamajame sąraše **Valiuta** pasirinkite anksčiau sukurtą klientų grupę.</span><span class="sxs-lookup"><span data-stu-id="a061d-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="a061d-145">Išplečiamajame sąraše **Adresų knygelės** pasirinkite esamą kliento adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="a061d-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="a061d-146">Pasirinkite **Įrašyti**, kad įrašytumėte ir grįžtumėte į naujo kliento informacijos ekraną.</span><span class="sxs-lookup"><span data-stu-id="a061d-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="a061d-147">Nebūtina įtraukti numatytojo kliento adreso.</span><span class="sxs-lookup"><span data-stu-id="a061d-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="a061d-148">Toliau pateiktame vaizde parodytas kliento kūrimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a061d-148">The following image shows an example of customer creation.</span></span>

![Numatytojo kliento kūrimas](media/default-customer-creation.png)

<span data-ttu-id="a061d-150">Toliau pateiktame vaizde parodytas numatytojo kliento konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="a061d-150">The following image shows a default customer configuration.</span></span>

![Kliento konfigūravimo pavyzdys](media/default-customer-configuration1.png)

<span data-ttu-id="a061d-152">Dauguma numatytųjų verčių kliento informacijos ekrane gali likti, bet dvi vertes reikia pakeisti.</span><span class="sxs-lookup"><span data-stu-id="a061d-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="a061d-153">Kliento informacijos ekrane išplėskite **Pardavimo užsakymo numatytieji nustatymai**.</span><span class="sxs-lookup"><span data-stu-id="a061d-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="a061d-154">Išplečiamajame sąraše **Svetainė** pasirinkite arba įveskite iš anksto sukonfigūruotą svetainę.</span><span class="sxs-lookup"><span data-stu-id="a061d-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="a061d-155">Išplečiamajame sąraše **Sandėlis** pasirinkite arba įveskite iš anksto sukonfigūruotą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="a061d-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="a061d-156">Toliau pateiktame vaizde parodytas kliento konfigūravimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a061d-156">The following image shows an example customer configuration.</span></span>

![Kliento konfigūravimo pavyzdys](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="a061d-158">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a061d-158">Additional resources</span></span>

[<span data-ttu-id="a061d-159">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="a061d-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a061d-160">Kanalo sąrankos būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="a061d-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)
