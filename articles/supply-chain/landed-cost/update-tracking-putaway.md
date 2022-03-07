---
title: Naujinti atidėjimo stebėjimą
description: Šioje temoje aprašoma, kaip nustatyti ir paleisti periodinės užduoties Naujinimo atidėjimo stebėjimą.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d8e2a42d8e12a5a9cf18e876b6f9e45ecb877881
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500028"
---
# <a name="update-tracking-for-put-away"></a>Naujinti atidėjimo stebėjimą

[!include [banner](../includes/banner.md)]

*Naujinti sekimo stebėjimą* periodinei užduočiai yra sukurtas vykdyti kaip naktinė pasikartojanti užduotis. Joje nurodoma, kurie reisai gavo visas atsargų operacijas ir kurie reisai neturi vertės faktinei pabaigos datai. Tada, jei reikia, ji nustato faktinę pabaigos datą į dabartinę datą.

*Konteinerio veiklos* yra sukuriamos kiekvienam veiklos ciklo *etapui* kiekvienam *pristatymo konteineriui*. Šios vertės apibrėžiamos pagal veiklos ciklo šabloną, kuris pasirenkamas sukūrus reisą. Kiekviename konteinerio veiklos įraše vertės gali būti nustatytos **Pradžios data**, **Numatyta pabaigos data** ir **Faktinė pabaigos data** laukeliuose. Šiuos laukus galima atnaujinti, kai gaunamas patvirtinimas, kad etapas buvo pradėtas arba užbaigtas.

Paprastai informaciją, susijusią su patvirtintomis datomis, pateikia trečioji šalis, pvz., krovinių ekspeditoriai, nes šie veiksmai prižiūrimi ne Microsoft Dynamics 365 Supply Chain Management. Tačiau iš trečiosios šalies gauta informacija nereikalauja sekti prekių iš veiklos ciklo etapoatvykimo į sandėlį (kaip pažymėta prekių atidėjime). Todėl sekimą galima nustatyti pagal informaciją, esamą Dynamics 365 Supply Chain Management.

Kaip nustatyti ir paleisti periodinės užduoties *Atnaujinimo atidėjimo stebėjimą*, sekite šiuos veiksmus:

1. Eikite į **Pakrovimo išlaidos \> Periodinės užduotys \>Atnaujinimo stebėjimo atidėjimas**.
1. Dialogo lange **Atnaujinti stebėjimo atidėjimą**, **Parametrai** skyriuje nustatykite šiuos laukus:

    - **Etapas** – pasirinkti unikalų identifikavimo pavadinimą/veiklos ciklo, kuriam norite atnaujinti sekimą, dalies numerį. Pasirinkta vertė turi nurodyti reiso atvykimą į sandėlį.
    - **Veikla** – pasirinkite veiklą, kuri buvo atlikta pasirinktos atkarpos metu. Šios vertės priskiriamos pagal veiklos ciklo šablono eilutę sekimo kontrolės centre.

1. Norėdami apriboti įrašų, kurie turi būti įtraukti į atnaujinimą, rinkinį, "FastTab" **Įtraukti įrašus** pasirinkite **Filtravimo** mygtuką. Atsiranda standartinis užklausos dialogo langas, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ fono užduočių tipams. Laukų informaciją galima tik skaityti ir vertes, susijusias su jūsų užklausa.
1. „FastTab” **Vykdyti fone** nustatykite paketo ir planavimo parinktis taip, kaip jums reikia, kaip ir kitiems „Supply Chain Management” užduočių tipams.
1. Pasirinkite **OK**, jei norite pritaikyti parametrus, ir norėdami paleisti arba suplanuoti atnaujinimą.
