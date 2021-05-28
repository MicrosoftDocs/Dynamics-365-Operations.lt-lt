---
title: Paskutinio patikrintos datos laukas nėra atnaujinamas, kai sukuriami keli kokybės užsakymai
description: Paskutinio patikrintos datos laukas nėra atnaujinamas, kai sukuriami keli kokybės užsakymai.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f796bdaa88d32b1c58dd8a4bca19f0ce4f3943d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026756"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Paskutinio patikrintos datos laukas nėra atnaujinamas, kai sukuriami keli kokybės užsakymai

KB numeris: 4612803

## <a name="symptoms"></a>Požymiai

Laukas **paskutinio patikrintos dato** nėra atnaujinamas, kai sukuriami keli kokybės užsakymai.

## <a name="resolution"></a>Skiriamoji geba

Sistema veikia kaip sukurta. Paskutinė patikrinta data nėra susijusi su kokybės užsakymais. Joje saugoma data, kada baigtos prekės pirmą kartą buvo nupirktos arba pagamintos. Ši data naudojama apskaičiuojant pranešimo apie laikymo trukmę datą.
