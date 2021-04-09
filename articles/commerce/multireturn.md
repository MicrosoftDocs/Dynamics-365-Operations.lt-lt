---
title: Kelių klientų užsakymų ir sąskaitų faktūrų grąžinamos prekės
description: Šioje temoje aprašomos funkcijos, padedančios atlikti kelių klientų užsakymų ir SF grąžinimus „Dynamics 365 Commerce“.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796902"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Kelių klientų užsakymų ir sąskaitų faktūrų grąžinamos prekės

[!include [banner](includes/banner.md)]


Šiame straipsnyje aprašomos dvi funkcijos, optimizuojančios kliento užsakymų grąžinimą naudojant kelias sąskaitas faktūras. 

## <a name="enable-refunds-over-multiple-captures"></a>Įjungti grąžinimą už kelis patvirtinimus

Šia funkcija įgalinami keli susieti to paties kliento užsakymo grąžinimai. 

1. Eikite į darbo sritį **Funkcijų valdymas** ir ieškokite **Įjungti grąžinimą už kelis patvirtinimus**.
2. Pasirinkite **Įjungti grąžinimą už kelis užsakymus** ir spustelėkite **Įjungti**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Įjungti tinkamą mokesčių skaičiavimą, kai grąžinamas dalinis kiekis

Šia funkcija užtikrinama, kad užsakymą grąžinus naudojant kelias sąskaitas faktūras, galiausiai mokesčiai bus lygūs pirminei mokėtinai mokesčių sumai. 

1. Eikite į darbo sritį **Funkcijų valdymas** ir ieškokite **Įjungti tinkamą mokesčių skaičiavimą, kai grąžinamas dalinis kiekis**.
2. Pasirinkite **Įjungti tinkamą mokesčių skaičiavimą, kai grąžinamas dalinis kiekis** ir spustelėkite **Įjungti**. 


## <a name="process-returns"></a>Grąžinimų apdorojimas

Įjungus šias funkcijas ir pakeitimus sinchronizavus su parduotuvėmis, parduotuvės kasininkas gali pasirinkti kelis kliento pardavimo užsakymus dėl grąžinimo.

Pasirinkus užsakymus, bus parodytas visų grąžintinų produktų iš visų užsakymų SF sąrašas. Tada kasininkas gali pasirinkti grąžintinus produktus. Sukuriamas vienas grąžinimo užsakymas visiems pasirinktiems produktams.

Jei grąžintas visas užsakymas, klientui grąžinta mokesčių suma bus lygi pirminei mokėtinai mokesčių sumai.



[!INCLUDE[footer-include](../includes/footer-banner.md)]