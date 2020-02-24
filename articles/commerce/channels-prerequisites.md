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
# <a name="channel-setup-prerequisites"></a>Būtinosios kanalo nustatymo sąlygos


[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ būtinųjų kanalo nustatymo sąlygų apžvalga.

## <a name="overview"></a>Peržiūrėti

Prieš sukuriant „Dynamics 365 Commerce“ kanalą reikia atlikti keletą būtinųjų užduočių. Šie būtinųjų užduočių sąrašai organizuojami pagal kanalo tipą.

> [!NOTE]
> Kai kurie dokumentai vis dar rašomi, o saitai bus atnaujinti, kai bus publikuojamas naujas turinys.

## <a name="initialization"></a>Inicializacija

- [Pradinių duomenų inicijavimas](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Visuotinės visų kanalų tipų būtinosios sąlygos

- [Juridinio subjekto apibrėžimas ir konfigūravimas](channels-legal-entities.md) 
- [Organizacijos hierarchijos konfigūravimas](channels-org-hierarchies.md)
- [Sandėlio nustatymas](channels-setup-warehouse.md)
- [PVM konfigūravimas](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [El. paštu siunčiamo pranešimo šablono nustatymas](email-notification-profiles.md)
- [Numeracijų nustatymas](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Numatytojo kliento ir adresų knygelės nustatymas](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Būtinosios mažmeninės prekybos kanalo sąlygos

- [Informacijos kodai ir informacijos kodų grupės](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Mažmeninės prekybos funkcijų šablono nustatymas](retail-functionality-profile.md)
- [Darbuotojų adresų knygelės nustatymas](new-address-book.md)
- [Ekrano maketo nustatymas](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Aparatūros stoties nustatymas](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Skambučių centro kanalo būtinosios sąlygos

- Skambučių centro parametrai
- Skambučių centro grąžinimo metodai
- Nuomos tipai
- Mokėjimo tarnybos
- Užsakymo sulaikymo kodai

## <a name="online-channel-prerequisites"></a>Būtinosios interneto kanalo sąlygos

- [Internetinių funkcijų šablono kūrimas](online-functionality-profile.md)

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų apžvalga](channels-overview.md)

[Organizacijų ir organizacijų hierarchijų apžvalga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organizacijų hierarchijų nustatymas](channels-org-hierarchies.md)

[Juridinių subjektų kūrimas](channels-legal-entities.md)

[Mažmeninės prekybos kanalo nustatymas](channel-setup-retail.md)
    
[Interneto kanalo nustatymas](channel-setup-online.md)
