---
title: Kelių klientų užsakymų ir SF grąžinamos prekės
description: Šioje temoje aprašomos funkcijos, kurios leidžia atlikti kelių klientų užsakymų ir SF „Microsoft Dynamics 365 for Retail“ grąžinimus.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: d410fde2cd127f8d644e6a385937b6bc98d74576
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517127"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Kelių klientų užsakymų ir SF grąžinamos prekės

[!include [banner](includes/banner.md)]


„Dynamics 365 for Finance and Operations“ 10.0 versijoje galima atlikti kelių užsakymų ir SF grąžinimus, kai senesnėse nei 10.0 versijose vienu metu galima apdoroti tik vienos SF grąžinimus. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Konfigūruokite „Retail“, kad būtų palaikomi kelių kliento užsakymų ir SF grąžinimai

1. Eikite į **„Retail“ parametrai \> Klientų užsakymai**.
1. Įjunkite parametrą **Įjungti kelių užsakymų grąžinimus**. 

## <a name="process-returns"></a>Grąžinimų apdorojimas

Įjungus šį parametrą ir pakeitimus sinchronizavus su parduotuvėmis, parduotuvės kasininkas gali pasirinkti kelis kliento pardavimo užsakymus dėl grąžinimo.

Pasirinkus užsakymus, bus parodytas visų grąžintinų produktų iš visų užsakymų SF sąrašas. Tada kasininkas gali pasirinkti grąžintinus produktus. Sukuriamas vienas grąžinimo užsakymas visiems pasirinktiems produktams.
