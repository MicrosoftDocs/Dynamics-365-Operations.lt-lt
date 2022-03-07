---
title: Prekybos sutarties sąlygos netaikomas importuoto užsakymo eilutėms
description: Prekybos sutarčių kainos ir nuolaidos netaikomos pardavimo arba pirkimo užsakymo eilutėse, kurios importuojamos naudojant duomenų valdymą
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477120"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Prekybos sutarties sąlygos netaikomas importuoto užsakymo eilutėms

## <a name="symptoms"></a>Požymiai

Prekybos sutartys, taikytinos pardavimo arba pirkimo užsakymo eilutėse nėra taikomos eilutėse, kurios importuojamos naudojant duomenų valdymą. Tačiau tos pačios prekybos sutartys yra taikomos pardavimo arba pirkimo užsakymo eilutėms, sukurtoms rankiniu būdu.

## <a name="cause"></a>Priežastis

Jei pirkimo užsakymo eilutėse, kurios importuojamos naudojant duomenų tvarkymą, jau yra informacija apie kainą, prekybos sutartis nebus iš naujo įvertinta tose eilutėse. Pavyzdžiui, jei **Eilutės nuolaidos procentas** arba bet kuri iš kainų ir nuolaidų verčių nustatoma eilutei, tada prekybos sutarčių nebus ieškoma toje eilutėje.

## <a name="workaround"></a>Apėjimo būdas

Tikimasi tokio elgesio ir jis yra panašus tiek pardavimo, tiek pirkimo užsakymuose.

Kaip sprendimą, importuokite pirkimo užsakymo eilutes nenurodydami jokios kainos informacijos. Tada bus taikomos prekybos sutartys, o pirkimo užsakymo eilutės bus atnaujintos remiantis apibrėžtomis prekybos sutartimis.
