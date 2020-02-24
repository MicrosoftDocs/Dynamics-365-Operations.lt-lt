---
title: Hibridiniai kliento užsakymai
description: Hibridinis kliento užsakymas yra vienas užsakymas, apimantis produktus, kuriuos klientas gali išsinešti iš parduotuvės pats, ir produktus, kurie bus paimti arba išsiųsti vėliau.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1c2105aa99e0489d7643d076e84123eec628679e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023487"
---
# <a name="hybrid-customer-orders"></a>Hibridiniai kliento užsakymai

[!include [banner](includes/banner.md)]

Hibridinis kliento užsakymas yra vienas užsakymas, apimantis produktus, kuriuos klientas gali išsinešti iš parduotuvės pats, ir produktus, kurie bus paimti arba išsiųsti vėliau.

Programoje „Commerce“ galite pasirinkti išsinešti visus arba pasirinktus kliento užsakymo produktus. Sukūrus užsakymą automatiškai išrašoma SF už produktų eilutes, pažymėtas išsinešti; tai taip pat taikoma užsakymui, kurio produktai bus paimti po užsakymo sukūrimo. Hibridinių užsakymų mokėtina suma nustatoma sudėjus paimtinų ir siųstinų produktų eilučių depozito procentą ir visą išsinešti pažymėtų produktų eilučių sumą. Kai naudojami hibridiniai užsakymai, sistema perjungia kliento užsakymo režimą ir atsiskaitymo grynaisiais režimą, kaip nurodyta toliau.

- Jei visi produktai krepšelyje yra nustatyti kaip **Išsineština**, užsakymas bus tvarkomas kaip atsiskaitymo grynaisiais operacija.
- Jei visos ar bent viena eilutė krepšelyje yra nustatyti kaip **Paimtina** arba **Išsiųstina**, užsakymas bus tvarkomas kaip kliento užsakymo operacija.

Pasirinkus krepšelio eilutę ir parinktį **Išrinkti pasirinktus**, **Išsiųsti pasirinktus** arba **Išsinešti pasirinktus**, toks pristatymo būdas nustatomas tik konkrečiai krepšelio eilutei. Tokiu atveju operacijos proceso pabaigos srautas tęsiamas įprastai. Tačiau, jei pažymėta parinktis **Išrinkti pasirinktus**, **Išsiųsti pasirinktus** arba **Išsinešti pasirinktus**, bet nepasirinkta jokia krepšelio eilutė, atidaromas naujas puslapis, kuriame pateikiamos visos krepšelio eilutės. Tame ekrane galite vienu metu pasirinkti kelias eilutes ir nustatyti jų pristatymo būdą. Pritaikius tą būdą pasirinktoms eilutėms, perrašomas bet koks ankstesnis toms eilutėms priskirtas pristatymo būdas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Klientų užsakymai naudojant „Modern POS“ (MPOS)](customer-orders-overview.md)
