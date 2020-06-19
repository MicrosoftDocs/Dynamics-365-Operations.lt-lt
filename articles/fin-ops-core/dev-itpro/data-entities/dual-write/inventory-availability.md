---
title: Atsargų pasiekiamumas dvigubam rašymui
description: Šioje temoje pateikiama informacija apie atsargų pasiekiamumo tikrinimą dvigubo rašymo funkcijoje.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426987"
---
# <a name="inventory-availability"></a>Atsargų pasiekiamumas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Naudodami atsargų pasiekiamumą, galite patikrinti savo atsargas prieš įtraukdami produktą į formas **Pasiūlymai**, **Užsakymai** arba **Sąskaitos-faktūros** modeliu grįstose programose programoje „Dynamics 365“. Pavyzdžiui, atsargų ir įvykdymo datos tikrinimas yra pagrindinė [potencialių klientų pavertime grynaisiais pinigais](dual-write-prospect-to-cash.md) proceso užduotis. Jeigu nepakanka atsargų, galite įvertinti pristatymo datą pagal suplanuotų atsargų gavimą ir išdavimą. Taip pat galite patikrinti produkto prieinamų atsargų (ATP) informaciją, kurioje galima rasti ATP kiekį iš anksto apibrėžtame laikotarpyje.

## <a name="on-hand-inventory"></a>Turimos atsargos 

„Dynamics 365 Sales“ formų **Pasiūlymai**, **Užsakymai** arba **Sąskaitos faktūros** antraštėje įtraukiamas mygtukas **Turimos atsargos**. Spustelėjus mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę ir produktą, kurio turimas atsargas norite patikrinti. Jis pateikia atsargų informaciją iš „Dynamics 365 Supply Chain Management“ ir parodo tokią pačią informaciją kaip [Turimos atsargos](../../../../supply-chain/inventory/tasks/check-availability-stock.md). Informaciją sudaro šie kiekiai:

- **Turimas kiekis**
- **Rezervuotas turimas kiekis**
- **Pasiekiamas turimas kiekis**
- **Užsakytas kiekis**
- **Užsakymo kiekis**
- **Rezervuotas užsakytas kiekis**
- **Visas pasiekiamas kiekis**

## <a name="atp-information"></a>ATP informacija

„Dynamics 365 Sales“ formų **Pasiūlymai**, **Užsakymai** arba **Sąskaitos faktūros** antraštės internetiniuose elementuose įtraukiamas mygtukas **ATP informacija**. Spustelėjus mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę, produktą, atsargų svetainę, atsargų sandėlį ir užsakymo kiekį. Jis pateikia **ATP informaciją** iš „Supply Chain Management“ ir parodo parametrus, aprašytus [Užsakymų vykdymo perspektyva](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations). Informaciją sudaro **ATP kiekis**, **Gaunamas kiekis**, **Išduodamas kiekis**ir **Turimas kiekis**.
