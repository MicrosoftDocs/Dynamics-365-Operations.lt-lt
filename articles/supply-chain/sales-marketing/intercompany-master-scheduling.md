---
title: Vidinės įmonės bendrasis planavimas
description: Šioje temoje paaiškinamas vidinės įmonės bendrasis planavimas
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 02d1a3675cfe30f2e72237f69509398122d17f05
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671876"
---
# <a name="intercompany-master-scheduling"></a>Vidinės įmonės bendrasis planavimas

[!include [banner](../../includes/banner.md)]

Vidinės įmonės bendrasis planavimas yra priemonė, kurią naudodami keliose vidinėse įmonėse skaičiuojate poreikius ir generuojate suplanuotus vidinės įmonės užsakymus. Vidinės įmonės bendrasis planavimas vykdomas kartojant tiek kartų, kiek nurodote. Norėdami įgalinti „Microsoft Dynamics 365 Supply Chain Management“ atlikti vidinės įmonės bendrąjį planavimą, jį turite nustatyti kiekvienoje vidinei įmonei priklausančioje įmonėje. Todėl vykdomi keli pakartojimai, kurių metu „Microsoft Dynamics 365 Supply Chain Management“ automatiškai sukuria vidinės įmonės pirkimo užsakymą, o tai priverčia automatiškai sukurti vidinės įmonės pardavimo užsakymą, dėl kurio vėlgi atsiranda naujų poreikių.

Vidinės įmonės bendrąjį planą ir planavimo tvarką nustatote kiekvienos vidinės įmonės įmonės **Pagrindinis planavimas** parametruose.

Norėdami išplatinti poreikį visoje vidinės įmonės grandinėje, turite nustatyti parametrus, kurie užtikrintų automatinį suplanuotų pirkimo užsakymų patvirtinimą, t. y. negalima keisti užsakymo laiko arba kiekio. Padengimo **grupėje nustatykite** tvirtinto laiko ribas arba **Bendrojo plano tvirtinto** laiko ribas. Jei **Pasirašymo laiko tvora** nenustatytos, vidinės įmonės pirkimo užsakymai nebus kuriami automatiškai. Suplanuotus užsakymus lemia tik pirmasis bendrojo planavimo vykdymas. Tačiau, kadangi vidinės įmonės pirkimo užsakymas nėra sukurtas, vidinės įmonės pardavimo užsakymas nėra sukurtas, todėl daugiau vidinės įmonės pirkimo užsakymų nėra sukurta ir t. t.

Kai paleidžiate vidinės įmonės bendrąjį planavimą, „Microsoft Dynamics 365 Supply Chain Management“ kiekvienoje vidinei įmonei priklausančioje įmonėje atlieka po vieną bendrąjį planavimą tada kiekvienoje vidinei įmonei priklausančioje įmonėje atlieka antrą bendrąjį planavimą ir t. t., kol įvykdo nurodytą pakartojimų skaičių. Maksimalus galimas pakartojimų skaičius yra 30, bet kuo daugiau pakartojimų pasirenkate, tuo ilgiau užtrunka planavimas.

Vidinės įmonės bendrąjį planavimą galite pradėti nuo bet kurios vidinės įmonės, kadangi bendrąjį planavimą įmonėse kontroliuoja vidinės įmonės planavimo seka, t. y. tvarka, kuria programa nustato, kuriose vidinei įmonei priklausančiose įmonėse pirma turėtų būti atliekamas bendrasis planavimas, galite pradėti vidinės įmonės pagrindinį planavimą iš bet kurių vidinių įmonių. Kadangi vidinės įmonės planavimo seka nustato įmonėse atliekamo bendrojo planavimo tvarką, nesvarbu, kur pradedamas vidinės įmonės bendrasis planavimas. Kiekvieno pakartojimo metu esama įmonė tvarkoma paskutinė.

> [!NOTE]
> Geriausia būtų vidinės įmonės bendrąjį planavimą pradėti nuo vienoje „Microsoft Dynamics 365 Supply Chain Management“ įmonėje.

Formoje **Vidiniės įmonės pagrindinis planavimas** puslapyje, galite pradėti bendrojo planavimo seką, kuri pirmą kartą vykdo bendrąjį planavimą, naudodama poreikio skaičiavimo atnaujinimo principą, kurį pasirinkote taikyti pirmojo pakartojimo metu. Vėlesniuose pakartojimuose naudojamas antrinis principas, kurį pasirinkote kitam pakartojimui, šis principas taikomas, kol atliekamas nurodytas pakartojimų skaičius.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
