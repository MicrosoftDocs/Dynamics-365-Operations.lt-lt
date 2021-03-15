---
title: Pardavimo pasiūlymų trikčių diagnostika
description: Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo pasiūlymais.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974765"
---
# <a name="troubleshoot-sales-quotations"></a>Pardavimo pasiūlymų trikčių diagnostika

Šioje temoje aprašoma, kaip spręsti problemas, kurios gali kilti kol dirbate su pardavimo pasiūlymais.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Negaliu pakeisti pardavimo pasiūlymo pardavimų kiekio aptarnavimo prekei.

### <a name="issue-description"></a>Problemos aprašas

Jei pardavimo pasiūlymo eilutėje bandysite nustatyti prekės, kurios tipas yra *Paslauga*, pardavimų kiekį (**SalesQty** laukas), jūs gausite tokį pranešimą: „Atnaujinimas neleidžiamas kiekio laukui.“

### <a name="issue-resolution"></a>Problemos paaiškinimas

Negalite nustatyti produktų, kurie yra aptarnavimo prekės, pardavimų kiekio. Pavyzdžiui, jei jūs siūlote paslaugą prekei įdiegti, nėra prasminga įrašyti kiekį, nes nėra faktinių prekių. Yra tik paslauga.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]