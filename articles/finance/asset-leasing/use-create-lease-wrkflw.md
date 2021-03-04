---
title: Nuomos patvirtinimo darbo eigų naudojimas
description: Šioje temoje paaiškinama, kaip naudoti darbo eigas, norint patvirtinti turto nuomą ir kaip stebėti darbo eigos būseną ir retrospektyvą.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1805e1f87ee70a1f35d9105b8f7ad6c95861efcc
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446207"
---
# <a name="use-lease-approval-workflows"></a>Nuomos patvirtinimo darbo eigų naudojimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudoti darbo eigas, norint patvirtinti turto nuomą ir kaip stebėti darbo eigos būseną ir retrospektyvą. Darbo eigos padeda suderinti nuomos patvirtinimų valdymą, suteikiant standartinį patvirtinimo priemonių rinkinį ir priskiriant konkrečius vartotojus, tvirtinančius kiekvieną proceso žingsnį. Tvirtintojas gali patvirtinti nuomą, jį atmesti, prašyti pakeisti arba priskirti jį kitam vartotojui patvirtinti. Be to, darbo eigos gali būti geriau matomos patvirtinimo procese, nes jūs sekate savo būseną ir retrospektyvą. Be to, galite peržiūrėti centralizuotą užduočių sąrašą, kuriame išvardijamos užduotys ir patvirtinimai, priskiriami konkretiems tvirtintojams.

Prieš pradėdami naudoti šią procedūrą, įsitikinkite, kad buvo sukurta bent jau nuomos patvirtinimo darbo eiga. Jei nėra darbo eigos, sukurkite ją. Informacijos apie tai, kaip nustatyti darbo eigą, ieškokite [Nuomos tvirtinimo darbo eigų nustatymas](set-up-lease-wrkflw.md).

1. Pateikite nuomą patvirtinti. Nuomos puslapyje **Knygos informacija** pasirinkite **Darbo eiga**, tada pasirinkite **Pateikti**.
2. Pasirodžiusiame dialogo lange galite pridėti komentarą. Nurodytas tvirtintojas matys šį komentarą kartu su nuoma. Baigę įvesti komentarą pasirinkite **Pateikti**. Nuoma pateikiama darbo eigos sistemai, o tvirtintojas jį gauna tvirtinti.
3. Norėdami peržiūrėti nuomos sutartis, kurias jie paskirti tvirtinti, pasirinkite **Moduliai \> Bendra \> Darbo elementai \> Man priskirti darbo elementai**.
4. Puslapyje **Man priskirti darbo elementai** pasirinkite nuomos, kurią norite peržiūrėti, saitą **Nuomos ID**. Rodomas puslapis priklauso nuo nuomos knygų ir nuomos informacijos, su kuria jūs turite prieigą.
5. Pabaigę peržiūrėti nuomą, pasirinkite **Darbo eiga** ir nuspręskite, kokių veiksmų reikia imtis. Parinktys: **Tvirtinti**, **Atmesti**, **Prašyti pakeisti**, **Perduoti** ir **Atšaukti**. Taip pat galite pasirinkti **Peržiūrėti retrospektyvą**, kad peržiūrėtumėte pasirinktos nuomos patvirtinimo retrospektyvą.
6. Pasirinkę veiksmą, įveskite komentarą, kuris aprašys veiksmą. Kai baigiate rašyti komentarą, sąraše pasirinkite veiksmą **Patvirtinta**.
7. Norėdami peržiūrėti patvirtinimo veiksmus, vėl atidarykite puslapį **Nuomos informacija** iš puslapio **Nuomos suvestinė** ir pasirinkite **Darbo eiga \> Rodinio retrospektyva**.

    Galite peržiūrėti darbo eigos veiklą darbo puslapyje **Darbo eigos retrospektyva**. Šiame puslapyje parodomi darbo eigos veiksmai, kurių buvo imtasi konkrečioje nuomos sutartyje. Norėdami peržiūrėti priskirtų darbo elementų būsenas, taip pat galite naudoti lauką **Darbo elementai**.

8. Norėdami išjungti darbo eigą, puslapyje **Darbo eigos retrospektyva** pasirinkite **Atšaukti**. Pasirodžiusiame dialogo lange įveskite komentarą, tada pasirinkite **Gerai**.
9. Norėdami išjungti darbo eigą arba suaktyvinti anksčiau sukurtą darbo eigą, pasirinkite **Turto nuoma \> Sąranka \> Nuomos darbo eiga**. Tada puslapyje **Nuomos darbo eiga** pasirinkite **Darbo eiga \> Versijos**. Norėdami, kad dabartinė darbo eiga būtų neaktyvi, pasirinkite aktyvią nuomos ir nuomos versijos dialogo langą ir pasirinkite **Išjungti**. Norėdami suaktyvinti esamą darbo eigą, pasirinkite darbo eigą ir pasirinkite **Suaktyvinti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]