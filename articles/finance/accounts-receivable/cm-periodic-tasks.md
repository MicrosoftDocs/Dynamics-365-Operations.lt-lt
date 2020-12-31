---
title: Periodinės kredito valdymo užduotys
description: Šioje temoje aprašomos periodinės užduotys, kurios yra būtina klientų kredito limitų valdymo proceso dalis.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 17b4b2f487fdeb9f1aa7d77bf87197885ba60e47
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445956"
---
# <a name="periodic-credit-management-tasks"></a>Periodinės kredito valdymo užduotys

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos periodinės užduotys, kurios yra būtina klientų kredito limitų valdymo proceso dalis.

## <a name="update-risk-scores"></a>Naujinti rizikos rezultatus

Kai verslas vystosi ir pasikeičia aplinkybės, tam tikro kliento kredito rizika taip pat gali pasikeisti. Norėdami padėti išlaikyti atitinkamus savo klientų kreditų limitus, turite periodiškai peržiūrėti kiekvieno rizikos balo kriterijus ir atnaujinti kiekvieno kliento balus. Galite atnaujinti šiuos balus puslapyje **Naujinti rizikos balus** (**Kreditai ir mokėjimų priežiūra \> Periodinės užduotys \> Kreditų valdymas \> Naujinti rizikos balus**). Visi vartotojo apibrėžti skaičiavimai taip pat apdorojami.

- **Vidutinės mokėjimo dienos** – šis balas yra vidutinis dienų, per kurias klientas turi apmokėti SF, skaičius.
- **Klientas nuo datos** – šis balas yra metų, kuriuos klientas yra jūsų organizacijos klientas, skaičius.
- **Vykdo verslą nuo** – šis balas yra metų, kuriuos klientas vykdo verslą, skaičius. Tai naudoja lauko **Verslo pradžios data** puslapyje **Klientai** reikšmę.
- **Neapmokėto pardavimo dienos** – šis balas yra paremtas gautinų sumų balansu, pardavimo įplaukomis ir dienų skaičiumi per ankstesnį 12 mėnesių laikotarpį.
- **Vidutinis balansas** – šis balas paremtas gautinų sumų balansu per ankstesnį 12 mėnesių laikotarpį.
- **Kredito valdymo grupė**, **Sąskaitų būsena** ir **Šalis** – šie balai naudoja kliento informaciją.

## <a name="update-customer-balance-statistics"></a>Kliento balanso statistikos naujinimas

Galite vykdyti procesą **Kliento balanso statistikos naujinimas** norėdami atnaujinti balanso statistikos, rodomos puslapyje **Balanso statistikos užklausos**, skaičiavimą. Ši informacija naudojama norint apskaičiuoti rizikos balus ir reikšmes, kurios rodomos statistikos „FactBox“ puslapyje **Klientas**.

Paleidus procesą, jis atnaujina vieno kliento balanso statistiką. Norėdami nustatyti paketines užduotis, kad būtų galima vykdyti procesą keliems klientams, galite naudoti puslapį **Skaičiuoti balanso statistiką** (**Kreditų valdymas \> Periodinės užduotys \> Skaičiuoti balanso statistiką**).
