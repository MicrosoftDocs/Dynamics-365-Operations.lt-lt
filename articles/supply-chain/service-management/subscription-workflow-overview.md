---
title: Abonemento darbo eigos peržiūra
description: Šioje temoje apžvelgiama abonemento darbo eiga.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5cff6910dcb273fc081443546676426387f6625
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "321644"
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

  


