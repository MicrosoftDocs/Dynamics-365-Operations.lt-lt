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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414469"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="a77bf-103">Internetinio funkcionalumo profilio kūrimas</span><span class="sxs-lookup"><span data-stu-id="a77bf-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a77bf-104">Šioje temoje apžvelgiamas internetinio funkcionalumo profilio nustatymas, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="a77bf-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a77bf-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="a77bf-105">Overview</span></span>

<span data-ttu-id="a77bf-106">Internetiniame funkcionalumo profilyje pateikiami įvairūs internetinių kanalų parametrai.</span><span class="sxs-lookup"><span data-stu-id="a77bf-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="a77bf-107">Kiekvienas internetinis kanalas turi nurodyti internetinį funkcionalumo profilį.</span><span class="sxs-lookup"><span data-stu-id="a77bf-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="a77bf-108">Internetinio funkcionalumo profilio kūrimas</span><span class="sxs-lookup"><span data-stu-id="a77bf-108">Create an online functionality profile</span></span>

<span data-ttu-id="a77bf-109">Toliau paaiškinama, kaip sukurti internetinį funkcionalumo profilį, naudojant „Commerce“ būstinės programą.</span><span class="sxs-lookup"><span data-stu-id="a77bf-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="a77bf-110">Naršymo srityje eikite į **Moduliai \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcionalumo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="a77bf-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="a77bf-111">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="a77bf-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a77bf-112">Lauke **Profilis** įveskite profilio ID.</span><span class="sxs-lookup"><span data-stu-id="a77bf-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="a77bf-113">Lauke **Aprašymas** įveskite vertę (toliau nurodytame paveikslėlyje„Adventure Works Profile“).</span><span class="sxs-lookup"><span data-stu-id="a77bf-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="a77bf-114">Skyriuje **Funkcijos**, jei reikia, pakeiskite nustatymus **KREPŠELIS**, **MAŽMENINĖS PREKYBOS KLIENTAI** arba **UŽBAIGTI PIRKIMĄ**.</span><span class="sxs-lookup"><span data-stu-id="a77bf-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="a77bf-115">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a77bf-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a77bf-116">Toliau parodytame paveikslėlyje pavaizduotas internetinio funkcionalumo profilio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a77bf-116">The following image shows an example online functionality profile.</span></span>
  
![Internetinio funkcionalumo profilio pavyzdys](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="a77bf-118">Funkcijos</span><span class="sxs-lookup"><span data-stu-id="a77bf-118">Functions</span></span>

- <span data-ttu-id="a77bf-119">**Sujungti produktus**: įjungus šią funkciją, krepšelis gali atnaujinti kiekį, kai ta pati prekė pridedama kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="a77bf-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="a77bf-120">**Leisti atlikti mokėjimą neapmokant už prekes**: įjungus šią funkciją apdorojamas scenarijus, kai į krepšelį dedamų prekių kaina yra 0,00 USD.</span><span class="sxs-lookup"><span data-stu-id="a77bf-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="a77bf-121">**Kurti klientą asinchroniniu režimu**: tai yra senesnis parametras, taikomas trečiųjų šalių „e-Commerce“ kanalams ir netaikomas „Dynamics 365“ „e-Commerce“ svetainei.</span><span class="sxs-lookup"><span data-stu-id="a77bf-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a77bf-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a77bf-122">Additional resources</span></span>

[<span data-ttu-id="a77bf-123">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="a77bf-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a77bf-124">Kanalo sąrankos būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="a77bf-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a77bf-125">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a77bf-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="a77bf-126">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a77bf-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="a77bf-127">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a77bf-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
