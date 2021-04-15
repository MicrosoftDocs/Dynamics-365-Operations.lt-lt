---
title: Mažmeninės prekybos funkcijų šablono kūrimas
description: Šioje temoje aprašoma, kaip sukurti funkcionalumo profilį, naudojant „Microsoft Dynamics 365 Commerce“.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792003"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="61b32-103">Mažmeninės prekybos funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="61b32-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61b32-104">Šioje temoje aprašoma, kaip sukurti funkcionalumo profilį, naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="61b32-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="61b32-105">Prekybos funkcionalumo profilyje pateikiami įvairūs interneto kanalų parametrai.</span><span class="sxs-lookup"><span data-stu-id="61b32-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="61b32-106">Kiekvienas kanalas turi nurodyti funkcionalumo profilį.</span><span class="sxs-lookup"><span data-stu-id="61b32-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="61b32-107">Kurti funkcijų šabloną</span><span class="sxs-lookup"><span data-stu-id="61b32-107">Create a functionality profile</span></span>

<span data-ttu-id="61b32-108">Norėdami sukurti funkcionalumo profilį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="61b32-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="61b32-109">Naršymo srityje eikite į **Moduliai \> Kanalo sąranka \> EKA profiliai \> Funkcionalumo profiliai**.</span><span class="sxs-lookup"><span data-stu-id="61b32-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="61b32-110">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="61b32-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="61b32-111">Lauke **Profilis** įveskite profilio ID (toliau nurodytame paveikslėlyje „FN006“).</span><span class="sxs-lookup"><span data-stu-id="61b32-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="61b32-112">Lauke **Aprašymas** įveskite vertę (toliau nurodytame paveikslėlyje„Adventure Works Profile“).</span><span class="sxs-lookup"><span data-stu-id="61b32-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="61b32-113">Skyriuje **Bendra** pasirinkite **ISO** lokalės šalį.</span><span class="sxs-lookup"><span data-stu-id="61b32-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="61b32-114">Skyriuje **Bendra** pakeiskite, jei reikia, kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="61b32-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="61b32-115">Skyriuje **Bendra** el. pašto kvitams pasirinkite **Kvito profilio ID**.</span><span class="sxs-lookup"><span data-stu-id="61b32-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="61b32-116">Jei reikia, skyriuje **Funkcijos** pakeiskite kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="61b32-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="61b32-117">Jei reikia, skyriuje **Suma** pakeiskite nustatymus.</span><span class="sxs-lookup"><span data-stu-id="61b32-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="61b32-118">Jei reikia, skyriuje **Informacijos kodai** pakeiskite kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="61b32-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="61b32-119">Jei reikia, skyriuje **Kvitų numeravimas** pakeiskite kitus nustatymus.</span><span class="sxs-lookup"><span data-stu-id="61b32-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="61b32-120">Toliau pateiktame vaizde parodytas funkcionalumo profilio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="61b32-120">The following image shows an example functionality profile.</span></span>
  
![Funkcionalumo profilio pavyzdys](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="61b32-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="61b32-122">Additional resources</span></span>

[<span data-ttu-id="61b32-123">Informacijos kodai ir informacijos kodų grupės</span><span class="sxs-lookup"><span data-stu-id="61b32-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="61b32-124">Naujos adresų knygos kūrimas</span><span class="sxs-lookup"><span data-stu-id="61b32-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="61b32-125">Ekrano maketo apžvalga</span><span class="sxs-lookup"><span data-stu-id="61b32-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="61b32-126">Konfigūruoti ir diegti „Retail Hardware Station“</span><span class="sxs-lookup"><span data-stu-id="61b32-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
