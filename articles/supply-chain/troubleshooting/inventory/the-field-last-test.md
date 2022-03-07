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
ms.openlocfilehash: 46523c55f4fd42b0985397752f0c62a3e1a55e177f2308e20b7064e339758269
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742033"
---
# <a name="the-last-tested-date-field-isnt-updated-when-multiple-quality-orders-are-created"></a>Paskutinio patikrintos datos laukas nėra atnaujinamas, kai sukuriami keli kokybės užsakymai

KB numeris: 4612803

## <a name="symptoms"></a>Požymiai

Laukas **paskutinio patikrintos dato** nėra atnaujinamas, kai sukuriami keli kokybės užsakymai.

## <a name="resolution"></a>Skiriamoji geba

Sistema veikia kaip sukurta. Paskutinė patikrinta data nėra susijusi su kokybės užsakymais. Joje saugoma data, kada baigtos prekės pirmą kartą buvo nupirktos arba pagamintos. Ši data naudojama apskaičiuojant pranešimo apie laikymo trukmę datą.
