---
title: Būtinosios kanalo nustatymo sąlygos
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.
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
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002294"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="62d75-103">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="62d75-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="62d75-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="62d75-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="62d75-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="62d75-105">Overview</span></span>

<span data-ttu-id="62d75-106">Prieš sukuriant „Dynamics 365 Commerce“ kanalą reikia atlikti keletą būtinųjų užduočių.</span><span class="sxs-lookup"><span data-stu-id="62d75-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="62d75-107">Šie būtinųjų užduočių sąrašai organizuojami pagal kanalo tipą.</span><span class="sxs-lookup"><span data-stu-id="62d75-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="62d75-108">Kai kurie dokumentai vis dar rašomi, o saitai bus atnaujinti, kai bus publikuojamas naujas turinys.</span><span class="sxs-lookup"><span data-stu-id="62d75-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="62d75-109">Inicializacija</span><span class="sxs-lookup"><span data-stu-id="62d75-109">Initialization</span></span>

- [<span data-ttu-id="62d75-110">Pradinių duomenų inicijavimas</span><span class="sxs-lookup"><span data-stu-id="62d75-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="62d75-111">Visuotinės visų kanalų tipų būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="62d75-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="62d75-112">Juridinio subjekto apibrėžimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="62d75-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="62d75-113">Organizacijos hierarchijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="62d75-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="62d75-114">Sandėlio nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="62d75-115">PVM konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="62d75-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="62d75-116">El. paštu siunčiamo pranešimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="62d75-117">Numeracijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="62d75-118">Numatytojo kliento ir adresų knygelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="62d75-119">Būtinosios mažmeninės prekybos kanalo sąlygos</span><span class="sxs-lookup"><span data-stu-id="62d75-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="62d75-120">Informacijos kodai ir informacijos kodų grupės</span><span class="sxs-lookup"><span data-stu-id="62d75-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="62d75-121">Mažmeninės prekybos funkcijų šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="62d75-122">Darbuotojų adresų knygelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="62d75-123">Ekrano maketo nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="62d75-124">Aparatūros stoties nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="62d75-125">Skambučių centro kanalo būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="62d75-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="62d75-126">Skambučių centro parametrai</span><span class="sxs-lookup"><span data-stu-id="62d75-126">Call center parameters</span></span>
- <span data-ttu-id="62d75-127">Skambučių centro grąžinimo metodai</span><span class="sxs-lookup"><span data-stu-id="62d75-127">Call center refund methods</span></span>
- <span data-ttu-id="62d75-128">Nuomos tipai</span><span class="sxs-lookup"><span data-stu-id="62d75-128">Rental types</span></span>
- <span data-ttu-id="62d75-129">Mokėjimo tarnybos</span><span class="sxs-lookup"><span data-stu-id="62d75-129">Payment services</span></span>
- <span data-ttu-id="62d75-130">Užsakymo sulaikymo kodai</span><span class="sxs-lookup"><span data-stu-id="62d75-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="62d75-131">Būtinosios interneto kanalo sąlygos</span><span class="sxs-lookup"><span data-stu-id="62d75-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="62d75-132">Internetinių funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="62d75-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="62d75-133">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="62d75-133">Additional resources</span></span>

[<span data-ttu-id="62d75-134">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="62d75-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="62d75-135">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="62d75-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="62d75-136">Organizacijų hierarchijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="62d75-137">Juridinių subjektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="62d75-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="62d75-138">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="62d75-139">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="62d75-139">Set up an online channel</span></span>](channel-setup-online.md)
