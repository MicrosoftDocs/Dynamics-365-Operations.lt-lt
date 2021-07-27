---
title: Abonemento darbo eigos peržiūra
description: Šioje temoje apžvelgiama abonemento darbo eiga.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca9ad7bb7a14652f31b3cde4448b983a43436d6c
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336322"
---
# <a name="subscription-workflow-overview"></a>Abonemento darbo eigos peržiūra 

[!include [banner](../includes/banner.md)]


Esate apšvietimo įmonės, kuri siūlo apšvietimo bokšto aptarnavimo abonementus, administratorius. Klientas kreipiasi į jūsų įmonę norėdamas pirkti apšvietimo bokšto aptarnavimo abonementą metams.

## <a name="setting-up-subscriptions"></a>Abonementų nustatymas

Norėdami nustatyti abonementą, pirmiausia turite sukurti naują aptarnavimo sutarties abonemento grupę arba patikrinti, ar yra abonemento grupė. Jei abonemento grupė yra, turite nustatyti ją taip, kad klientui kas metus būtų išrašoma SF ir kiekvieną metų mėnesį būtų kaupiamos pardavimo įplaukos. Daugiau informacijos apie tai, kaip nustatyti abonementus, ieškokite [Abonementų grupių nustatymas](set-up-subscription-groups.md).

Sukūrę abonementų grupę galite sukurti patį abonementą. Daugiau informacijos apie tai, kaip sukurti aptarnavimo abonementus, ieškokite [Aptarnavimo abonementų kūrimas naudojant abonementų grupę](create-service-subscriptions-from-subscription-group.md).

## <a name="create-and-modify-subscription-transactions"></a>Sukurkite ir modifikuokite abonementines operacijas

Nustatę abonementą, galite sukurti abonementinio mokesčio operaciją pirmajam apskaitomam laikotarpiui, kuris yra vieneri metai. Operacijų tipas – **Įprastas**. Todėl galite sukurti tik tas abonementines operacijas, kurių pradžios ir pabaigos datos atitinka laikotarpius, anksčiau sukurtus formoje **Laikotarpių tipai**. Daugiau informacijos apie mokesčių operacijas ieškokite [Abonementinio mokesčio operacijų kūrimas](create-subscription-fee-transactions.md).

Nustatę kliento abonementą prisimenate, kad susitarėte dėl 10 procentų nuolaidos visoms nustatytoms aptarnavimo pasiūlymų kainoms. Todėl turite sumažinti sukurto operacijos mokesčio kainą.

Vėliau jūsų kliento kontaktinis asmuo paskambinęs praneša, kad vis dar nori sudaryti apšvietimo bokšto aptarnavimo sutartį, bet naują apšvietimo bokštą planuoja pristatyti vėliau tais pačiais metais. Todėl jiems aptarnavimas reikalingas tik iki 2013 m. spalio mėn. Norėdami sumažinti kliento abonemento mėnesių skaičių, sukuriate naują abonemento mokesčio operaciją, paremtą pagal tipą **Sumažinimo dienos**. Daugiau informacijos apie tai, kaip sumažinti dienų, ieškokite [Abonementinio mokesčio dienų sumažinimas](reduce-the-days-on-subscription-fees.md).

## <a name="invoice-and-accrue-subscription-transactions"></a>Išrašykite SF ir kaupkite abonementines operacijas

Nustatėte abonementą ir esate pasiruošę už tai savo klientui išrašyti SF. Daugiau informacijos apie tai, kaip už abonementus išrašyti SF, ieškokite [Abonementinės operacijos, kurioms išrašyta SF](invoice-subscription-transactions.md).

Po dviejų dienų jūsų klientas paskambina ir praneša, kad SF už abonementą reikia išrašyti JAV doleriais, o ne eurais. Todėl sukuriate kredito pažymą ir naują abonementinę operaciją tinkama valiuta. Daugiau informacijos apie tai, kaip kredituoti abonementines operacijas, ieškokite [Abonementinių operacijų kreditavimas](credit-subscription-transactions.md).

Kiekvieno mėnesio pabaigoje vieno mėnesio kliento abonemento įplaukas galima sukaupti pelno ir nuostolių sąskaitoje bei NG sąskaitose. Daugiau informacijos apie tai, kaip sukaupti abonementų įplaukas, ieškokite [Abonemento įplaukų kaupimas](accrue-subscription-revenue.md).

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]