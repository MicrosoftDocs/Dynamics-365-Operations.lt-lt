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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477929"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="ecc1e-103">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="ecc1e-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ecc1e-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="ecc1e-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ecc1e-105">Prieš sukuriant „Dynamics 365 Commerce“ kanalą reikia atlikti keletą būtinųjų užduočių.</span><span class="sxs-lookup"><span data-stu-id="ecc1e-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="ecc1e-106">Šie būtinųjų užduočių sąrašai organizuojami pagal kanalo tipą.</span><span class="sxs-lookup"><span data-stu-id="ecc1e-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="ecc1e-107">Kai kurie dokumentai vis dar rašomi, o saitai bus atnaujinti, kai bus publikuojamas naujas turinys.</span><span class="sxs-lookup"><span data-stu-id="ecc1e-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="ecc1e-108">Inicializacija</span><span class="sxs-lookup"><span data-stu-id="ecc1e-108">Initialization</span></span>

- [<span data-ttu-id="ecc1e-109">Pradinių duomenų inicijavimas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="ecc1e-110">Visuotinės visų kanalų tipų būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="ecc1e-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="ecc1e-111">Juridinio subjekto apibrėžimas ir konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="ecc1e-112">Organizacijos hierarchijos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="ecc1e-113">Sandėlio nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="ecc1e-114">PVM konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ecc1e-115">El. paštu siunčiamo pranešimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="ecc1e-116">Numeracijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="ecc1e-117">Numatytojo kliento ir adresų knygelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="ecc1e-118">Būtinosios mažmeninės prekybos kanalo sąlygos</span><span class="sxs-lookup"><span data-stu-id="ecc1e-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="ecc1e-119">Informacijos kodai ir informacijos kodų grupės</span><span class="sxs-lookup"><span data-stu-id="ecc1e-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="ecc1e-120">Mažmeninės prekybos funkcijų šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="ecc1e-121">Darbuotojų adresų knygelės nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="ecc1e-122">Ekrano maketo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="ecc1e-123">Aparatūros stoties nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="ecc1e-124">Skambučių centro kanalo būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="ecc1e-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="ecc1e-125">Skambučių centro parametrai</span><span class="sxs-lookup"><span data-stu-id="ecc1e-125">Call center parameters</span></span>
- [<span data-ttu-id="ecc1e-126">Skambučių centro užsakymo ir grąžinimo mokėjimo būdai</span><span class="sxs-lookup"><span data-stu-id="ecc1e-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="ecc1e-127">Skambučių centro pristatymo ir mokesčių konfigūravimo būdai</span><span class="sxs-lookup"><span data-stu-id="ecc1e-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="ecc1e-128">Būtinosios interneto kanalo sąlygos</span><span class="sxs-lookup"><span data-stu-id="ecc1e-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="ecc1e-129">Internetinių funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="ecc1e-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ecc1e-130">Additional resources</span></span>

[<span data-ttu-id="ecc1e-131">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ecc1e-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ecc1e-132">Organizacijų ir organizacijų hierarchijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ecc1e-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ecc1e-133">Organizacijų hierarchijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="ecc1e-134">Juridinių subjektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="ecc1e-135">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="ecc1e-136">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecc1e-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
