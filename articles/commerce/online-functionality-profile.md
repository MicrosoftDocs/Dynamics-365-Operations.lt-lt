---
title: Internetinio funkcionalumo profilio kūrimas
description: Šioje temoje aprašoma, kaip sukurti internetinį funkcionalumo profilį, naudojant „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477737"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="3bd82-103">Internetinių funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="3bd82-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3bd82-104">Šioje temoje apžvelgiamas internetinio funkcionalumo profilio nustatymas, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="3bd82-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3bd82-105">Internetiniame funkcionalumo profilyje pateikiami įvairūs internetinių kanalų parametrai.</span><span class="sxs-lookup"><span data-stu-id="3bd82-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="3bd82-106">Kiekvienas internetinis kanalas turi nurodyti internetinį funkcionalumo profilį.</span><span class="sxs-lookup"><span data-stu-id="3bd82-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="3bd82-107">Internetinio funkcionalumo profilio kūrimas</span><span class="sxs-lookup"><span data-stu-id="3bd82-107">Create an online functionality profile</span></span>

<span data-ttu-id="3bd82-108">Toliau paaiškinama, kaip sukurti internetinį funkcionalumo profilį, naudojant „Commerce“ būstinės programą.</span><span class="sxs-lookup"><span data-stu-id="3bd82-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="3bd82-109">Naršymo srityje eikite į **Moduliai \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcionalumo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="3bd82-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="3bd82-110">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="3bd82-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="3bd82-111">Lauke **Profilis** įveskite profilio ID.</span><span class="sxs-lookup"><span data-stu-id="3bd82-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="3bd82-112">Lauke **Aprašymas** įveskite vertę (toliau nurodytame paveikslėlyje„Adventure Works Profile“).</span><span class="sxs-lookup"><span data-stu-id="3bd82-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="3bd82-113">Skyriuje **Funkcijos**, jei reikia, pakeiskite nustatymus **KREPŠELIS**, **MAŽMENINĖS PREKYBOS KLIENTAI** arba **UŽBAIGTI PIRKIMĄ**.</span><span class="sxs-lookup"><span data-stu-id="3bd82-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="3bd82-114">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3bd82-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="3bd82-115">Toliau parodytame paveikslėlyje pavaizduotas internetinio funkcionalumo profilio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3bd82-115">The following image shows an example online functionality profile.</span></span>
  
![Internetinio funkcionalumo profilio pavyzdys](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="3bd82-117">Funkcijos</span><span class="sxs-lookup"><span data-stu-id="3bd82-117">Functions</span></span>

- <span data-ttu-id="3bd82-118">**Sujungti produktus**: įjungus šią funkciją, krepšelis gali atnaujinti kiekį, kai ta pati prekė pridedama kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="3bd82-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="3bd82-119">**Leisti atlikti mokėjimą neapmokant už prekes**: įjungus šią funkciją apdorojamas scenarijus, kai į krepšelį dedamų prekių kaina yra 0,00 USD.</span><span class="sxs-lookup"><span data-stu-id="3bd82-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="3bd82-120">**Kurti klientą asinchroniniu režimu**: tai yra senesnis parametras, taikomas trečiųjų šalių „e-Commerce“ kanalams ir netaikomas „Dynamics 365“ „e-Commerce“ svetainei.</span><span class="sxs-lookup"><span data-stu-id="3bd82-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3bd82-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3bd82-121">Additional resources</span></span>

[<span data-ttu-id="3bd82-122">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="3bd82-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3bd82-123">Kanalo sąrankos būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="3bd82-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="3bd82-124">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="3bd82-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="3bd82-125">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="3bd82-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="3bd82-126">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="3bd82-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
