---
title: Turimų atsargų sąrašo puslapio filtravimo darbas nefiltruoja rezultatų, kurių tikėtasi
description: Filtro srities filtrai Turimas sąrašas puslapyje nefiltruoja rezultatų, kurių tikitės.
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
ms.openlocfilehash: df11b1c1e7de36fa0458cd931d4be7f84a15d143
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477121"
---
# <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-work-as-expected"></a>Turimų atsargų sąrašo puslapio filtravimo darbas nefiltruoja rezultatų, kurių tikėtasi

## <a name="symptoms"></a>Požymiai

Filtro srities filtrai **Turimas sąrašas**  puslapyje nefiltruoja rezultatų, kurių tikitės.

## <a name="resolution"></a>Sprendimas

Puslapis  **Turimas sąrašas** sudėliotas iš detalizuotos turimų atsargų lentelės, kurioje pateiktos visos galimos dimensijos. Nepaisant to, sąrašas šiame puslapyje santrauka. Dėl to, tai gali apimti eilutes iš šaltinio lentelės apimant vertes pagal rodomas dimensijas.

Filtrai, nustatyti filtrų srityje, taikomi šaltinio lentelei, tačiau ne apibendrintam sąrašui. Šis veikimas kartais gali lemti netikėtus rezultatus kaip nurodyta [šiuose pavyzdžiuose](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#examples).

Tačiau  [tinklelyje pateikti filtrai](/dynamics365/supply-chain/inventory/inventory-on-hand-list.md#grid-filters) *atlikti*  taikomas apibendrintam sąrašui. Šie filtrai apima tiek „QuickFilter“ tinklelio viršuje, tiek filtrą kiekvieno stulpelio antraštėje.
