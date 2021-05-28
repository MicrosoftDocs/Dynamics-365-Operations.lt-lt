---
title: Kelios paketo numerių atsargų operacijos, kai išjungtas faktinis atnaujinimas
description: Koreguous prekių, kurių paketo numerių grupės pasirinktis Faktiškai atnaujinus nustatyta kaip Ne, pirkimo užsakymo eilutę sukuriamos kelios atsargų operacijos.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026759"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Kelios paketo numerių atsargų operacijos, kai išjungtas faktinis atnaujinimas

KB numeris: 4613390

## <a name="symptoms"></a>Požymiai

Koreguous prekių, kurių paketo numerių grupės pasirinktis Faktiškai atnaujinus nustatyta kaip **Ne pirkimo užsakymo** eilutę sukuriamos kelios atsargų *operacijos*.

Kai kuriate prekę, kurios **paketo numerių grupės** pasirinktis Faktinis atnaujinimas nustatyta kaip *Ne*, sistema automatiškai sukuria naują paketo numerį, jei modifikuojate pirkimo eilutės kiekį ir išsaugote pirkimo užsakymo puslapį.

## <a name="resolution"></a>Skiriamoji geba

Paketo **numerių grupių faktinio** atnaujinimo parametras veikia taip:

- Kai pasirinktis nustatyta kaip *Taip*, nauji paketo numeriai kuriami tik po faktinio atnaujinimo (pvz., kai prekės siunčiamos arba gautos).
- Kai pasirinktis nustatyta kaip *Ne*, kaskart, kai taikomas atnaujinimas, sukuriamas naujas paketo numeris (pavyzdžiui, kai prie pirkimo užsakymo pridedamas naujas kiekis).
