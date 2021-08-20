---
title: Pasirinkus naują partijos ID paketo numeris išvalomas
description: Peržiūrint išrinkimo dokumento žurnalo eilutę, lauke Paketo numeris vertė išvaloma, jei lauke Partijos numeris pasirenkate naują vertę.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: datra
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d71720b1d3a34a31639db0f829dee300d6f96d53fd61c0a8740be9f2306d6dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738824"
---
# <a name="batch-number-is-cleared-when-a-new-lot-id-is-selected"></a>Pasirinkus naują partijos ID paketo numeris išvalomas

KB numeris: 4613107

## <a name="symptoms"></a>Požymiai

Peržiūrint išrinkimo dokumento žurnalo eilutę, lauke **Paketo numeris** vertė išvaloma, jei lauke **Partijos ID** pasirenkate naują vertę.

## <a name="resolution"></a>Skiriamoji geba

Sistema veikia kaip sukurta. Jei pakeisite partijos ID, pakeisite prekės kontekstą. Todėl paketo numeris yra atkurtas.

Norėdami susieti paketo numerį su partijos ID, pirmiausia turite nustatyti partijos ID.
