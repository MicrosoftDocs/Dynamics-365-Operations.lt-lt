---
title: "Hibridiniai kliento užsakymai"
description: "Hibridinis kliento užsakymas yra vienas užsakymas, apimantis produktus, kuriuos klientas gali išsinešti iš parduotuvės pats, ir produktus, kurie bus paimti arba išsiųsti vėliau."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1ddfc050cef94f4a31f5858b84c89eadfa726b95
ms.lasthandoff: 03/31/2017


---

# <a name="hybrid-customer-orders"></a>Hibridiniai kliento užsakymai

[!include[banner](includes/banner.md)]


Hibridinis kliento užsakymas yra vienas užsakymas, apimantis produktus, kuriuos klientas gali išsinešti iš parduotuvės pats, ir produktus, kurie bus paimti arba išsiųsti vėliau.

„Microsoft Dynamics 365 for Operations“ versijoje „Retail“ galite pasirinkti išsinešti visus arba pasirinktus kliento užsakymo produktus. Sukūrus užsakymą automatiškai išrašoma SF už produktų eilutes, pažymėtas išsinešti; tai taip pat taikoma užsakymui, kurio produktai bus paimti po užsakymo sukūrimo. Hibridinių užsakymų mokėtina suma nustatoma sudėjus paimtinų ir siųstinų produktų eilučių depozito procentą ir visą išsinešti pažymėtų produktų eilučių sumą. Kai naudojami hibridiniai užsakymai, sistema perjungia kliento užsakymo režimą ir atsiskaitymo grynaisiais režimą, kaip nurodyta toliau.

-   Jei visi produktai krepšelyje yra nustatyti kaip **Išsineština**, užsakymas bus tvarkomas kaip atsiskaitymo grynaisiais operacija.
-   Jei visos ar bent viena eilutė krepšelyje yra nustatyti kaip **Paimtina** arba **Išsiųstina**, užsakymas bus tvarkomas kaip kliento užsakymo operacija.

Pasirinkus krepšelio eilutę ir parinktį **Išrinkti pasirinktus**, **Išsiųsti pasirinktus** arba **Išsinešti pasirinktus**, toks pristatymo būdas nustatomas tik konkrečiai krepšelio eilutei. Tokiu atveju operacijos proceso pabaigos srautas tęsiamas įprastai. Tačiau, jei pažymėta parinktis **Išrinkti pasirinktus**, **Išsiųsti pasirinktus** arba **Išsinešti pasirinktus**, bet nepasirinkta jokia krepšelio eilutė, atidaromas naujas puslapis, kuriame pateikiamos visos krepšelio eilutės. Tame ekrane galite vienu metu pasirinkti kelias eilutes ir nustatyti jų pristatymo būdą. Pritaikius tą būdą pasirinktoms eilutėms, perrašomas bet koks ankstesnis toms eilutėms priskirtas pristatymo būdas.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kliento užsakymų apžvalga](customer-orders-overview.md)




