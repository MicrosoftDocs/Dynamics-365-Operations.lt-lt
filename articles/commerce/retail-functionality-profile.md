---
title: Mažmeninės prekybos funkcijų šablono kūrimas
description: Šioje temoje aprašoma, kaip sukurti funkcionalumo profilį, naudojant „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: 6bee51eb25b04eb65e588dd4cf54a0cef587aa15
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057353"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="b7813-103">Mažmeninės prekybos funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="b7813-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b7813-104">Šioje temoje aprašoma, kaip sukurti funkcionalumo profilį, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="b7813-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b7813-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="b7813-105">Overview</span></span>

<span data-ttu-id="b7813-106">Prekybos funkcionalumo profilyje pateikiami įvairūs interneto kanalų parametrai.</span><span class="sxs-lookup"><span data-stu-id="b7813-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="b7813-107">Kiekvienas kanalas turi nurodyti funkcionalumo profilį.</span><span class="sxs-lookup"><span data-stu-id="b7813-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="b7813-108">Kurti funkcijų šabloną</span><span class="sxs-lookup"><span data-stu-id="b7813-108">Create a functionality profile</span></span>

<span data-ttu-id="b7813-109">Norėdami sukurti funkcionalumo profilį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7813-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="b7813-110">Naršymo srityje eikite į **Moduliai \> Kanalo sąranka \> EKA profiliai \> Funkcionalumo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="b7813-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="b7813-111">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="b7813-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="b7813-112">Lauke **Profilis** įveskite profilio ID (toliau nurodytame paveikslėlyje „FN006“).</span><span class="sxs-lookup"><span data-stu-id="b7813-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="b7813-113">Lauke **Aprašymas** įveskite vertę (toliau nurodytame paveikslėlyje„Adventure Works Profile“).</span><span class="sxs-lookup"><span data-stu-id="b7813-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="b7813-114">Skyriuje **Bendra** pasirinkite **ISO** lokalės šalį.</span><span class="sxs-lookup"><span data-stu-id="b7813-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="b7813-115">Skyriuje **Bendra** pakeiskite, jei reikia, kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b7813-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="b7813-116">Skyriuje **Bendra** el. pašto kvitams pasirinkite **Kvito profilio ID**.</span><span class="sxs-lookup"><span data-stu-id="b7813-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="b7813-117">Jei reikia, skyriuje **Funkcijos** pakeiskite kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b7813-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="b7813-118">Jei reikia, skyriuje **Suma** pakeiskite nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b7813-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="b7813-119">Jei reikia, skyriuje **Informacijos kodai** pakeiskite kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b7813-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="b7813-120">Jei reikia, skyriuje **Kvitų numeravimas** pakeiskite kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b7813-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="b7813-121">Toliau pateiktame vaizde parodytas funkcionalumo profilio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="b7813-121">The following image shows an example functionality profile.</span></span>
  
![Funkcionalumo profilio pavyzdys](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="b7813-123">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b7813-123">Additional resources</span></span>

[<span data-ttu-id="b7813-124">Informacijos kodai ir informacijos kodų grupės</span><span class="sxs-lookup"><span data-stu-id="b7813-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="b7813-125">Naujos adresų knygos kūrimas</span><span class="sxs-lookup"><span data-stu-id="b7813-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="b7813-126">Ekrano maketo apžvalga</span><span class="sxs-lookup"><span data-stu-id="b7813-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="b7813-127">Konfigūruoti ir diegti „Retail Hardware Station“</span><span class="sxs-lookup"><span data-stu-id="b7813-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
