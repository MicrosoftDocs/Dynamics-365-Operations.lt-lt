---
title: "Hibridinis klientų užsakymus"
description: "Hibridinis kliento užsakymas yra vienetinį užsakymą, kuriame yra produktų, kurie gali būti vežami iš saugyklos klientui, taip pat produktų, kurie bus įlaipinami arba išsiųsti vėliau."
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

# <a name="hybrid-customer-orders"></a>Hibridinis klientų užsakymus

Hibridinis kliento užsakymas yra vienetinį užsakymą, kuriame yra produktų, kurie gali būti vežami iš saugyklos klientui, taip pat produktų, kurie bus įlaipinami arba išsiųsti vėliau.

Microsoft Dynamics 365 operacijų - mažmeninės prekybos, galite pasirinkti arba atlikti visus produktus arba atlikti išsirinktas prekes pirkėjo užsakyme. Eilutėms, kurios pažymėtos kaip atlikti automatiškai išrašytos sukūrus užsakymo produkto, taip pat tai yra tas pats išduoti vykdomąjį raštą, kuris turi būti įlaipinami veiksmų sukūrus užsakymo. Mokėtina suma hibridinių užsakymų nustatomas pridedant ir depozito procentinė išraiška pasirinkti ir laivo produktų linijas su linijos atlikti visą sumą. Hibridinis užsakymų, sistema pereina tarp klientų užsakymų ir atsiskaitoma grynaisiais režimo taip:

-   Jei visi produktai krepšelyje yra nustatytas kaip **atlikti pristatymo**, tvarka, bus tvarkoma kaip atsiskaitoma grynaisiais operaciją.
-   Jei bet kurios arba visų eilučių krepšelyje yra nustatytas kaip **pasirinkti** ar **laivo pristatymo**, tvarka, bus tvarkoma kaip kliento užsakymo operaciją.

Jei krepšelis linija pažymėtas ir **pasiimti pasirinktas**, **laivas pasirinktas**, arba **atlikti pasirinktas** yra pasirinkta, tik konkrečių krepšelis linija nustatoma šį pristatymo būdą. Tokiu atveju pasroviui atsirandančių srauto operacijos toliau kaip įprasta. Tačiau jei **pasiimti pasirinktas**, **laivas pasirinktas**, arba **atlikti pasirinktas** pažymėtas be krepšelio eilutės yra atrinkti, naujas puslapis atsidaro, kad išvardijamos visos krepšelio eilutės. Kad ekranas, galite pasirinkti kelias eilutes vienu metu nustatyti pristatymo būdą. Naudojant šį metodą pasirinkti eilutes, bet ankstesniais pristatymo būdą, kuris buvo priskirtas prie linijos bus nepaisoma.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Klientų užsakymų apžvalga](customer-orders-overview.md)


