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
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003377"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="fe307-103">Internetinio funkcionalumo profilio kūrimas</span><span class="sxs-lookup"><span data-stu-id="fe307-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fe307-104">Šioje temoje apžvelgiamas internetinio funkcionalumo profilio nustatymas, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="fe307-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fe307-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="fe307-105">Overview</span></span>

<span data-ttu-id="fe307-106">Internetiniame funkcionalumo profilyje pateikiami įvairūs internetinių kanalų parametrai.</span><span class="sxs-lookup"><span data-stu-id="fe307-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="fe307-107">Kiekvienas internetinis kanalas turi nurodyti internetinį funkcionalumo profilį.</span><span class="sxs-lookup"><span data-stu-id="fe307-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="fe307-108">Internetinio funkcionalumo profilio kūrimas</span><span class="sxs-lookup"><span data-stu-id="fe307-108">Create an online functionality profile</span></span>

<span data-ttu-id="fe307-109">Toliau paaiškinama, kaip sukurti internetinį funkcionalumo profilį, naudojant „Commerce“ būstinės programą.</span><span class="sxs-lookup"><span data-stu-id="fe307-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="fe307-110">Naršymo srityje eikite į **Moduliai \> Kanalo sąranka \> Interneto parduotuvės sąranka \> Funkcionalumo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="fe307-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="fe307-111">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="fe307-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="fe307-112">Lauke **Profilis** įveskite profilio ID.</span><span class="sxs-lookup"><span data-stu-id="fe307-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="fe307-113">Lauke **Aprašymas** įveskite vertę (toliau nurodytame paveikslėlyje„Adventure Works Profile“).</span><span class="sxs-lookup"><span data-stu-id="fe307-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="fe307-114">Skyriuje **Funkcijos**, jei reikia, pakeiskite nustatymus **KREPŠELIS**, **MAŽMENINĖS PREKYBOS KLIENTAI** arba **UŽBAIGTI PIRKIMĄ**.</span><span class="sxs-lookup"><span data-stu-id="fe307-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="fe307-115">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="fe307-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="fe307-116">Toliau parodytame paveikslėlyje pavaizduotas internetinio funkcionalumo profilio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="fe307-116">The following image shows an example online functionality profile.</span></span>
  
![Internetinio funkcionalumo profilio pavyzdys](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="fe307-118">Funkcijos</span><span class="sxs-lookup"><span data-stu-id="fe307-118">Functions</span></span>

- <span data-ttu-id="fe307-119">**Sujungti produktus**: įjungus šią funkciją, krepšelis gali atnaujinti kiekį, kai ta pati prekė pridedama kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="fe307-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="fe307-120">**Leisti atlikti mokėjimą neapmokant už prekes**: įjungus šią funkciją apdorojamas scenarijus, kai į krepšelį dedamų prekių kaina yra 0,00 USD.</span><span class="sxs-lookup"><span data-stu-id="fe307-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="fe307-121">**Kurti klientą asinchroniniu režimu**: tai yra senesnis parametras, taikomas trečiųjų šalių „e-Commerce“ kanalams ir netaikomas „Dynamics 365“ „e-Commerce“ svetainei.</span><span class="sxs-lookup"><span data-stu-id="fe307-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe307-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="fe307-122">Additional resources</span></span>

[<span data-ttu-id="fe307-123">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="fe307-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="fe307-124">Kanalo sąrankos būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="fe307-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="fe307-125">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="fe307-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="fe307-126">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="fe307-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="fe307-127">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="fe307-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)