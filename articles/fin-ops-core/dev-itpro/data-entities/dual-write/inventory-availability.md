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
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443877"
---
# <a name="inventory-availability-in-dual-write"></a>Atsargų pasiekiamumas dvigubam rašymui

[!include [banner](../../includes/banner.md)]

Naudodami atsargų pasiekiamumą, galite patikrinti savo atsargas prieš pridėdami produktą į **Kainos**, **Užsakymai** arba **Sąskaitos faktūros** puslapį „Microsoft Dynamics 365 Sales”. Pavyzdžiui, patikrinkite atsargas ir nustatykite įvykdymo datą kaip vieną iš pagrindinių užduočių [potencialaus grynųjų pinigų](dual-write-prospect-to-cash.md) proceso metu.

Jeigu nepakanka atsargų, galite įvertinti pristatymo datą pagal suplanuotų atsargų gavimą ir išdavimą. Taip pat galite patikrinti produkto prieinamų atsargų (ATP) informaciją, kurioje galima rasti ATP kiekį iš anksto apibrėžtoje laiko riboje.

## <a name="on-hand-inventory"></a>Turimos atsargos

„Dynamics 365 Sales“ naujas **Turimos atsargos** mygtukas pridėtas **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapių antraštėse. Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę ir produktą, kurio turimas atsargas norite patikrinti. Šis dialogo langas parodo tokią pačią informaciją kaip [Turimos atsargos](../../../../supply-chain/inventory/tasks/check-availability-stock.md).

Dialogo langas grąžina atsargų informaciją iš „Dynamics 365 Supply Chain Management”. Pateikiama informacija apie šiuos kiekius:

- Turimas kiekis
- Rezervuotas turimas kiekis
- Prieinamas turimas kiekis
- Užsakytas kiekis.
- Užsakymo kiekis
- Rezervuotas užsakytas kiekis
- Bendras prieinamas kiekis

## <a name="atp-information"></a>ATP informacija

„Sales” naujas **ATP informacija** mygtukas pridėtas prie eilutės elementų **Kainos**, **Užsakymai** ir **Sąskaitos faktūros** puslapiuose. Spustelėjus šį mygtuką, pasirodo dialogo langas, kuriame galite nurodyti įmonę, produktą, atsargų vietą, atsargų sandėlį ir užsakymo kiekį. Šis dialogo langas turi tuos pačius parametrus, aprašytus [Užsakymo vykdymo įsipareigojimuose](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).

Dialogo langas grąžina ATP informaciją iš „Supply Chain Management”. Pateikiama informacija apie šiuos kiekius:

- ATP kiekis
- Gavimo kiekis
- Išdavimo kiekis
- Turimas kiekis
