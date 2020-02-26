---
title: Slėpti ne vežėjo pristatymo būdus EKA siuntimo pasirinktyse
description: Šioje temoje aprašoma konfigūracijos parinktis, kuri neleidžia pasirinkti ne vežėjo pristatymo būdus, kai elektroninio kasos aparato (EKA) programoje kuriami siuntimo užsakymai.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 75e7e8f183982f7829db78eb75b8c29c9ab95e89
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023486"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Slėpti ne vežėjo pristatymo būdus EKA siuntimo pasirinktyse


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma konfigūracijos parinktis, kuri galima naudoti elektroninio kasos aparato (EKA) programoje. Ši konfigūracijos pasirinktis keičia pristatymo būdo pasirinkimo elgseną, kai EKA kuriami siuntimo užsakymai.

Vartotojai gali pasirinkti siuntos pristatymo būdą, kai kuria kliento siuntimo užsakymus EKA. Ši funkcija yra prieinama neatsižvelgiant į tai, ar siunčiamas visas užsakymas, ar tik pasirinktos eilutės.

Pagal numatytuosius nustatymus dialogo lange, kuriame pasirinktas pristatymo būdas, rodomi visi leistini pristatymo būdai, skirti kanalo, prekės ir pristatymo adreso kombinacijai. Šie pristatymo būdai apibrėžti „Headquarters” puslapyje **Pristatymo būdai** (**Pardavimas ir rinkodara \> Sąranka \> Platinimas \> Pristatymo būdai**). „Ne vežėjo” pristatymo būdai, pvz., **Išsineštinis** arba**Paėmimas**, taip pat gali būti pasirinkti dialogo lange.

Tačiau buvo įtraukta funkcija, leidžianti paslėpti ne vežėjo pristatymo būdus dialogo lange. Norėdami įjungti šią funkciją, puslapyje **Prekybos parametrai**, skirtuke **Kliento užsakymai**, nustatykite pasirinktį **Rodyti tik vežėjo pristatymo būdus, skirtus užsakymų siuntimui** į **Taip**. Įjungus šią funkciją ir vykdant atitinkamas paskirstymo užduotis, skirtas sinchronizuoti informaciją su kanalo duomenų baze, ne vežėjo pristatymo būdų nebus galima pasirinkti siuntimo užsakymų kūrimo EKA proceso metu.
