---
title: Funkciniai pertrūkiai tarp invenoriaus vertės/senėjimo ataskaitų ir jų laikymo versijų
description: Funkciniai pertrūkiai tarp invenoriaus vertės/senėjimo ataskaitų ir jų laikymo versijų
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a72e2d32e755e137cebbc0bf7afb0bed08fb93f2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477116"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Funkciniai pertrūkiai tarp invenoriaus vertės/senėjimo ataskaitų ir jų laikymo versijų

[Inventoriaus senėjimo ataskaitos laikymas](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage.md) ir [Inventoriaus vertės laikymo ataskaita](/dynamics365/supply-chain/cost-management/inventory-value-report-storage.md) funkcijos įjungimas „Supply Chain Management“ siekiant rodyti didelės apimties inventoriaus perlaidas. Visais atvejais, ataskaitos rezultatai yra įrašomi į naršymą ir eksportavimą, skirtingai nei šių ataskaitų nelaikymo versijos. Nepaisant to, kai kurios funkcijos esančio šių ataskaitų nelaikymo versijose neegzistuoja laikymo versijose. Tolesni papildomi skyriai apibendrina skirtumus ir pateikia apėjimus.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Laikymo ataskaitos neapiba papildomų tarpines sumos, net jei jos įjungtos ataskaitos išdėstyme.

Tarpinės sumos gali sukelti problemas, kai rezultatas yra eksportuojamas, ypač jei naudotojai keičia įrašo seką.

Norėdami patikrinti tarpines sumas, galite eksportuoti rezultatą į „Microsoft Excel“. Kitu atveju, norėdami patikrinti tarpines sumas „Supply Chain Management“ naudokite [Funkcijos valdymą](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad įjungtumėte funkcijas *Naujo tinklelio valdiklis* ir *Grupavimas į tinklelius*, suteikiančias lankstesnį būdą matyti tarpines sumas bet kuriai kitai stulpelio grupei. Norėdami gauti daugiau informacijos, žr. [Tinklelio galimybės](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities.md).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Inventoriaus vertės talpinimo ataskaita nepalaiko buhalterinės sąskaitos informacijos

Galite vykdyti bandyminį balansą tam, kad gautumėte inventoriaus sąskaitas ir palygintumėte jas su **Inventoriaus vertės laikymo** ataskaita.
