---
title: Kanalo siekiant naudoti kanalų naršymo hierarchiją konfigūravimas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukonfigūruoti kanalą siekiant naudoti kanalo naršymo hierarchiją.
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
ms.openlocfilehash: ceb6aa65c2ed5bc8d4224bdaf7095fba769181e8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220587"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="35148-103">Kanalo siekiant naudoti kanalų naršymo hierarchiją konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="35148-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="35148-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukonfigūruoti kanalą siekiant naudoti kanalo naršymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="35148-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35148-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="35148-105">Overview</span></span>

<span data-ttu-id="35148-106">Kanalo naršymo hierarchijos naudojamos, norint skirstyti produktus į kategorijas, kad produktus būtų galima naršyti el. prekybos svetainėje arba elektroniniame kasos aparate (EKA).</span><span class="sxs-lookup"><span data-stu-id="35148-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="35148-107">Mažmeninės prekybos ir internetiniai kanalai turi būti sukonfigūruoti naudojant kanalo naršymo hierarchijas.</span><span class="sxs-lookup"><span data-stu-id="35148-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="35148-108">Kanalo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="35148-108">Configure the channel</span></span>

<span data-ttu-id="35148-109">Norėdami sukonfigūruoti kanalą, kad būtų galima naudoti kanalo naršymo hierarchiją, atlikite tokius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="35148-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="35148-110">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalų kategorijos ir produktų atributai**.</span><span class="sxs-lookup"><span data-stu-id="35148-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="35148-111">Pasirinkite konfigūruotiną kanalą.</span><span class="sxs-lookup"><span data-stu-id="35148-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="35148-112">Veiksmų srityje pasirinkite **Nustatyti atributų metaduomenis**.</span><span class="sxs-lookup"><span data-stu-id="35148-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="35148-113">Išskleidžiamajame sąraše **Kategorijų hierarchija** pasirinkite atitinkamą kanalo naršymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="35148-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="35148-114">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="35148-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="35148-115">Dalyje **Atributų grupė** įtraukite bet kurias atributų grupes, kurios bus visų mazgų visuotiniai atributai.</span><span class="sxs-lookup"><span data-stu-id="35148-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="35148-116">Toliau pateiktame vaizde parodoma, kaip sukonfigūruoti kanalą, kad būtų galima naudoti kanalo naršymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="35148-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Kanalo konfigūravimo pavyzdys](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="35148-118">Nustatyti atributo metaduomenis</span><span class="sxs-lookup"><span data-stu-id="35148-118">Set attribute metadata</span></span>

<span data-ttu-id="35148-119">Nustačius atributų metaduomenis bus galima konfigūruoti kiekvieno mazgo atributus.</span><span class="sxs-lookup"><span data-stu-id="35148-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="35148-120">Norėdami nustatyti atributų metaduomenis, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="35148-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="35148-121">Veiksmų srityje pasirinkite **Nustatyti atributų metaduomenis**.</span><span class="sxs-lookup"><span data-stu-id="35148-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="35148-122">Kiekvienam mazgui pasirinkite **Kanalo produktų atributai**.</span><span class="sxs-lookup"><span data-stu-id="35148-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="35148-123">Nustatykite **Rodyti atributus kanale** į **Taip** ir **Galima patikslinti** į **Taip**, kad būtų įjungtos to kanalo tikslinimo priemonės.</span><span class="sxs-lookup"><span data-stu-id="35148-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="35148-124">Sukonfigūravę kiekvieną mazgą taip, kaip pageidaujate, **Veiksmų sritis** pasirinkite mygtuką **Įrašyti**, kad įrašytumėte.</span><span class="sxs-lookup"><span data-stu-id="35148-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="35148-125">Viršutiniame dešiniajame kampe pasirinkite **X**, kad išeitumėte iš šio ekrano ir grįžtumėte į puslapį **Kanalų kategorijos ir produktų atributai**.</span><span class="sxs-lookup"><span data-stu-id="35148-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="35148-126">Toliau pateiktame paveiksle parodyti kanalo produktų atributų, sukonfigūruotų kanalų kategorijos mazge, pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="35148-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanalo atributai kanalo kategorijos mazgo](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="35148-128">Keitimų publikavimas</span><span class="sxs-lookup"><span data-stu-id="35148-128">Publish changes</span></span>

<span data-ttu-id="35148-129">Kad atlikti pakeitimai įsigaliotų, turite juos publikuoti.</span><span class="sxs-lookup"><span data-stu-id="35148-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="35148-130">Norėdami publikuoti keitimus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="35148-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="35148-131">Veiksmų srityje pasirinkite **Publikuoti kanalo naujinimus**.</span><span class="sxs-lookup"><span data-stu-id="35148-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="35148-132">Veiksmų srityje **Publikuoti kanalo naujinimus** pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="35148-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="35148-133">Toliau pateiktame paveiksle parodyta, kaip publikuoti kanalo naujinimus.</span><span class="sxs-lookup"><span data-stu-id="35148-133">The following image shows how to publish channel updates.</span></span>

![Publikuoti kanalo naujinimus](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="35148-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="35148-135">Additional resources</span></span>

[<span data-ttu-id="35148-136">Kanalo naršymo hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="35148-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]