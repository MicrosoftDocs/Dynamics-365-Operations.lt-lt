---
title: Negalima nustatyti aptarnavimo prekių kiekio pardavimo pasiūlymo eilutėje
description: Dirbant su pardavimo pasiūlymais, negalima nustatyti produktų, kurie yra aptarnavimo prekės, pardavimo kiekio, nes nėra faktinių prekių, kurias būtų galima suskaičiuoti.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477133"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Negaliu keisti prekybos kiekio paslaugų prekei prekybos kainų eilutėje

## <a name="symptoms"></a>Požymiai

Jei pardavimo pasiūlymo eilutėje bandysite nustatyti prekės, kurios tipas yra *Paslauga*, pardavimų kiekį (**SalesQty** laukas), jūs gausite tokį pranešimą: „Atnaujinimas neleidžiamas kiekio laukui:

> Lauko Kiekis atnaujinti neleidžiama.

## <a name="cause"></a>Priežastis

Toks veikimo būdas yra numatytas. Negalite nustatyti produktų, kurie yra aptarnavimo prekės, pardavimų kiekio. Pavyzdžiui, jei jūs siūlote paslaugą prekei įdiegti, nėra prasminga įrašyti kiekį, nes nėra faktinių prekių yra skaičiuojamas. Yra tik paslauga.
