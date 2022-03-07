---
title: Slėpti ne vežėjo pristatymo būdus EKA siuntimo pasirinktyse
description: Šioje temoje aprašoma konfigūracijos parinktis, kuri neleidžia pasirinkti ne vežėjo pristatymo būdus, kai elektroninio kasos aparato (EKA) programoje kuriami siuntimo užsakymai.
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 4d885aa7ab3b4daaebb1fa8378562d86cc153270ea166b495bf3381fae826773
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773890"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Slėpti ne vežėjo pristatymo būdus EKA siuntimo pasirinktyse


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma konfigūracijos parinktis, kuri galima naudoti elektroninio kasos aparato (EKA) programoje. Ši konfigūracijos pasirinktis keičia pristatymo būdo pasirinkimo elgseną, kai EKA kuriami siuntimo užsakymai.

Vartotojai gali pasirinkti siuntos pristatymo būdą, kai kuria kliento siuntimo užsakymus EKA. Ši funkcija yra prieinama neatsižvelgiant į tai, ar siunčiamas visas užsakymas, ar tik pasirinktos eilutės.

Pagal numatytuosius nustatymus dialogo lange, kuriame pasirinktas pristatymo būdas, rodomi visi leistini pristatymo būdai, skirti kanalo, prekės ir pristatymo adreso kombinacijai. Šie pristatymo būdai apibrėžti „Headquarters” puslapyje **Pristatymo būdai** (**Pardavimas ir rinkodara \> Sąranka \> Platinimas \> Pristatymo būdai**). „Ne vežėjo” pristatymo būdai, pvz., **Išsineštinis** arba **Paėmimas**, taip pat gali būti pasirinkti dialogo lange.

Tačiau buvo įtraukta funkcija, leidžianti paslėpti ne vežėjo pristatymo būdus dialogo lange. Norėdami įjungti šią funkciją, puslapyje **Prekybos parametrai**, skirtuke **Kliento užsakymai**, nustatykite pasirinktį **Rodyti tik vežėjo pristatymo būdus, skirtus užsakymų siuntimui** į **Taip**. Įjungus šią funkciją ir vykdant atitinkamas paskirstymo užduotis, skirtas sinchronizuoti informaciją su kanalo duomenų baze, ne vežėjo pristatymo būdų nebus galima pasirinkti siuntimo užsakymų kūrimo EKA proceso metu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]