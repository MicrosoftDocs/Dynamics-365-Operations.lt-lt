---
title: Turimų atsargų sąrašo puslapio filtravimo darbas nefiltruoja rezultatų, kurių tikėtasi
description: Filtrai, filtruoti pagal puslapio "Turimas sąrašas" filtro sritį, nefiltruoti rezultatų, kaip tikitės.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 3857ce3720430c6f512d5abc4c9c4d390a0c3377
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686689"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Turimų atsargų sąrašo puslapio filtravimo darbas nefiltruoja rezultatų, kurių tikėtasi

## <a name="symptoms"></a>Požymiai

Turimos atsargų sąrašo puslapio filtrų **srities filtrai** filtruoja rezultatus, kaip tikitės.

## <a name="resolution"></a>Sprendimas

**Turimo sąrašo** puslapis yra sureguliuotas iš išsamaus turimo inventoriaus lentelės, kuri apima visas dimensijas. Nepaisant to, sąrašas šiame puslapyje santrauka. Dėl to, tai gali apimti eilutes iš šaltinio lentelės apimant vertes pagal rodomas dimensijas.

Filtrai, nustatyti filtro srityje, taikomi šaltinio lentelei, bet ne suvestinei sąrašui. Šis veikimas kartais gali lemti netikėtus rezultatus kaip nurodyta [šiuose pavyzdžiuose](/dynamics365/supply-chain/inventory/inventory-on-hand-list#examples).

Nepaisant to, [tinklelyje pateikti filtrai](/dynamics365/supply-chain/inventory/inventory-on-hand-list#grid-filters) *yra* taikomi apibendrintam sąrašui. Šie filtrai apima tiek „QuickFilter“ tinklelio viršuje, tiek filtrą kiekvieno stulpelio antraštėje.
