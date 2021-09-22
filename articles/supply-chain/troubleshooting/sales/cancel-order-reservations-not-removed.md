---
title: Atšaukus užsakymą rezervacijų pašalinti negalima
description: Negalite atšaukti prekybos užsakymo, kol susietas darbas su tuo užsakymu yra atšauktas ir grąžintas. Norėdami tai padaryti, atlikite toliau nurodytus tris veiksmus.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477103"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Atšaukus užsakymą rezervacijų pašalinti negalima

## <a name="symptoms"></a>Požymiai

Jei darbas susietas su pardavimo užsakymu ir bandote atšaukti šį užsakymą, gaunate tokį klaidos pranešimą:

> Rezervacijų šalinti negalima, nes sukurtas šiomis rezervacijomis grindžiamas darbas.

Negalite atšaukti prekybos užsakymo, kol susietas darbas su tuo užsakymu yra atšauktas ir grąžintas. Šis reikalavimas taikomas, net jei darbas, susietas su pardavimo užsakymu, yra uždarytas.

## <a name="resolution"></a>Sprendimas

Norėdami ištaisyti šią problemą, vykdykite toliau nurodytus veiksmus.

1. Atšaukite darbą ir grąžinkite atsargas į norimą vietą. Eikite prie atitinkamo pardavimo užsakymo krovinio ir pasirinkite arba **Sumažinti paimtą kiekį** krovinio eilutėje, arba **Atšaukti darbą** veiksmų srityje.

    Dabar darbo būsena yra *Atšaukta*, o naujas atsargų perkėlimo darbas automatiškai sukuriamas ir apdorojamas, siekiant sugrąžinti atsargas į vietą, kuri buvo aprašyta atšaukimo metu.

2. Panaikinkite krovinį. Siunta taip pat panaikinama.

3. Dabar turėtumėte galėti nueiti į pardavimo užsakymą ir jį atšaukti.
