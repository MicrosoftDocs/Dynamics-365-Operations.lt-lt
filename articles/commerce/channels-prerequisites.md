---
title: Būtinosios kanalo nustatymo sąlygos
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
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
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113787"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="82f4a-103">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="82f4a-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="82f4a-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="82f4a-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="82f4a-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="82f4a-105">Overview</span></span>

<span data-ttu-id="82f4a-106">Prieš sukuriant „Dynamics 365 Commerce“ kanalą reikia atlikti keletą būtinųjų užduočių.</span><span class="sxs-lookup"><span data-stu-id="82f4a-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="82f4a-107">Šie būtinųjų užduočių sąrašai organizuojami pagal kanalo tipą.</span><span class="sxs-lookup"><span data-stu-id="82f4a-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="82f4a-108">Kai kurie dokumentai vis dar rašomi, o saitai bus atnaujinti, kai bus publikuojamas naujas turinys.</span><span class="sxs-lookup"><span data-stu-id="82f4a-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="82f4a-109">Inicializacija</span><span class="sxs-lookup"><span data-stu-id="82f4a-109">Initialization</span></span>

- [<span data-ttu-id="82f4a-110">Pradinių duomenų inicijavimas</span><span class="sxs-lookup"><span data-stu-id="82f4a-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="82f4a-111">Visuotinės visų kanalų tipų būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="82f4a-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="82f4a-112">Juridinio subjekto apibrėžimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="82f4a-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="82f4a-113">Organizacijos hierarchijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="82f4a-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="82f4a-114">Sandėlio nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="82f4a-115">PVM konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="82f4a-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="82f4a-116">El. paštu siunčiamo pranešimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="82f4a-117">Numeracijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="82f4a-118">Numatytojo kliento ir adresų knygelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="82f4a-119">Būtinosios mažmeninės prekybos kanalo sąlygos</span><span class="sxs-lookup"><span data-stu-id="82f4a-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="82f4a-120">Informacijos kodai ir informacijos kodų grupės</span><span class="sxs-lookup"><span data-stu-id="82f4a-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="82f4a-121">Mažmeninės prekybos funkcijų šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="82f4a-122">Darbuotojų adresų knygelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="82f4a-123">Ekrano maketo nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="82f4a-124">Aparatūros stoties nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="82f4a-125">Skambučių centro kanalo būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="82f4a-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="82f4a-126">Skambučių centro parametrai</span><span class="sxs-lookup"><span data-stu-id="82f4a-126">Call center parameters</span></span>
- [<span data-ttu-id="82f4a-127">Skambučių centro užsakymo ir grąžinimo mokėjimo būdai</span><span class="sxs-lookup"><span data-stu-id="82f4a-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="82f4a-128">Skambučių centro pristatymo ir mokesčių konfigūravimo būdai</span><span class="sxs-lookup"><span data-stu-id="82f4a-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="82f4a-129">Būtinosios interneto kanalo sąlygos</span><span class="sxs-lookup"><span data-stu-id="82f4a-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="82f4a-130">Internetinių funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="82f4a-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="82f4a-131">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="82f4a-131">Additional resources</span></span>

[<span data-ttu-id="82f4a-132">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="82f4a-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="82f4a-133">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="82f4a-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="82f4a-134">Organizacijų hierarchijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="82f4a-135">Juridinių subjektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="82f4a-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="82f4a-136">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="82f4a-137">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="82f4a-137">Set up an online channel</span></span>](channel-setup-online.md)
