---
title: Būtinosios kanalo nustatymo sąlygos
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.
author: samjarawan
ms.date: 02/21/2020
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
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800524"
---
# <a name="channel-setup-prerequisites"></a>Būtinosios kanalo nustatymo sąlygos

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.

Prieš sukuriant „Dynamics 365 Commerce“ kanalą reikia atlikti keletą būtinųjų užduočių. Šie būtinųjų užduočių sąrašai organizuojami pagal kanalo tipą.

> [!NOTE]
> Kai kurie dokumentai vis dar rašomi, o saitai bus atnaujinti, kai bus publikuojamas naujas turinys.

## <a name="initialization"></a>Inicijavimas

- [Pradinių duomenų inicijavimas](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Visuotinės visų kanalų tipų būtinosios sąlygos

- [Juridinio subjekto apibrėžimas ir konfigūravimas](channels-legal-entities.md) 
- [Organizacijos hierarchijos konfigūravimas](channels-org-hierarchies.md)
- [Sandėlio nustatymas](channels-setup-warehouse.md)
- [PVM konfigūravimas](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [El. paštu siunčiamo pranešimo šablono nustatymas](email-notification-profiles.md)
- [Numeracijų nustatymas](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [Numatytojo kliento ir adresų knygelės nustatymas](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Būtinosios mažmeninės prekybos kanalo sąlygos

- [Informacijos kodai ir informacijos kodų grupės](info-codes-retail.md)
- [Mažmeninės prekybos funkcijų šablono nustatymas](retail-functionality-profile.md)
- [Darbuotojų adresų knygelės nustatymas](new-address-book.md)
- [Ekrano maketo nustatymas](pos-screen-layouts.md)
- [Aparatūros stoties nustatymas](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>Skambučių centro kanalo būtinosios sąlygos

- Skambučių centro parametrai
- [Skambučių centro užsakymo ir grąžinimo mokėjimo būdai](work-with-payments.md)
- [Skambučių centro pristatymo ir mokesčių konfigūravimo būdai](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>Būtinosios interneto kanalo sąlygos

- [Internetinių funkcijų šablono kūrimas](online-functionality-profile.md)

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų apžvalga](channels-overview.md)

[Organizacijų ir organizacijų hierarchijų apžvalga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organizacijų hierarchijų nustatymas](channels-org-hierarchies.md)

[Juridinių subjektų kūrimas](channels-legal-entities.md)

[Mažmeninės prekybos kanalo nustatymas](channel-setup-retail.md)
    
[Interneto kanalo nustatymas](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
