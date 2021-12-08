---
title: Sinchronizuoti vidinės įmonės kliento informaciją
description: Šioje temoje paaiškinamas vidinės įmonės užsakymų kliento informacijos sinchronizavimas
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548428"
---
# <a name="synchronize-intercompany-customer-information"></a>Sinchronizuoti vidinės įmonės kliento informaciją

[!include [banner](../../includes/banner.md)]

Kliento informacija sinchronizuojama, jei kuriant pardavimo užsakymą arba keičiant klientą, tiekėjo nuorodą arba kliento paraiškos numerį įgalintas laukas **Kliento informacija**.

Visada galite pakeisti šių sinchronizavimo laukų vertę. Tačiau pasirinkus šį parametrą, galima tik nustatyti, ar ši vertė nukopijuota į kitus vidinės įmonės užsakymus. Jei vidinės įmonės pardavimo užsakyme įgalinote lauką **Kliento informacija** vidinės įmonės pardavimo užsakymo pokytis yra sinchronizuojamas į vidinės įmonės pirkimo užsakymą. Jei vidinės įmonės pirkimo užsakyme taip pat įgalinote lauką **Kliento informacija** jis sinchronizuojamas atgal į pagrindinį pardavimo užsakymą.

> [!NOTE]
> Jei įgalinote laukus **Kliento informacija** ir vidinės įmonės pirkimo užsakyme, ir pardavimo užsakyme, atnaujinimai padaryti vieno žmogaus vienoje įmonėje yra panaikinami tame pačiame užsakyme kito žmogaus kitoje įmonėje padarytų atnaujinimų.

Geriausia vidinės įmonės pirkimo užsakyme **Kliento informacija** įgalinti kliento informacijos lauką. Tai įgalina sinchronizavimą tarp pradinio pardavimo užsakymo ir vidinės įmonės pirkimo užsakymo bei iš vidinės įmonės pirkimo užsakymo į vidinės įmonės pardavimo užsakymą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]