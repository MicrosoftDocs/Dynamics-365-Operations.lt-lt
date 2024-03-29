---
title: Periodinės kredito valdymo užduotys
description: Šiame straipsnyje aprašomos periodinės užduotys, kurios yra klientų kredito limitų valdymo proceso dalis.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9ad72463acba301f7fc931f9fe316a9a9758922e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888012"
---
# <a name="periodic-credit-management-tasks"></a>Periodinės kredito valdymo užduotys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos periodinės užduotys, kurios yra klientų kredito limitų valdymo proceso dalis.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
