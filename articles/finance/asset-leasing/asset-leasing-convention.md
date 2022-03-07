---
title: Turto nuomos sutartys
description: Šioje temoje aprašomos sutartys išnuomotam turtui.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: afc432d448f3b013dd8732120d7e8a50a9169343c705a75465e669156fd5e052
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740031"
---
# <a name="asset-leasing-conventions"></a>Turto nuomos sutartys

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje aprašomos sutartys išnuomotam turtui. Lizingo sutartys yra naudojamas nustatyti nuomos knygos pradžios datą. Jei lizingo sutartis yra nustatyta į **Jokia**, pradžios data yra tokia pati kaip nuomos pradžios data (tai reiškia, kad vertė yra **Nuomos pradžios datos** laukelio). Jei lizingo sutartis yra nustatyta į **Viso mėnesio**, pradžios data yra pirmoji mėnesio data, į kurį patenka nuomos pradžios data.

Pradžios datos nustato įsipareigojimų amortizavimo laikotarpio pradžios datą ir turto nuvertėjimo grafikus. Interesų išlaidos ir nuvertėjimo kaštai yra publikuojami atitinkamų grafikų laikotarpio pabaigos duomenimis. Pradinis pripažinimas ir koregavimo žurnalo įrašas yra publikuojami pradžios dieną.

> [!NOTE]
> Lizingo sutarčių funkcija turi būti įjungta per Funkcijų valdymą. Darbo srityje **Funkcijų valdymas** raskite ir pasirinkite funkciją pavadinimu **Lizingo sutartis turto nuomai** ir tada rinkitės **Įjungti dabar**.

Lizingo sutartys yra priskiriamos lizingo turto knygos nustatymui.

Norėdami peržiūrėti ir priskirti lizingo sutartį, atlikite šiuos žingsnius.

1. Eikite į **Turto nuoma \> Sąranka \> Nuomos knygos**.
2. Laukelyje **Lizingo sutartis** rinkitės vieną tolesnių verčių.

    | Nuomos konvencija | Aprašymas |
    |--------------------|-------------|
    | Nėra               | Įsipareigojimų amortizavimo ir turto nuvertėjimo grafikai prasideda nuomos pradžios dieną, nes pradžios data atitinka nuomos pradžios datą. Pabaigos data yra vienu mėnesiu vėliau. Ši lizingo sutarti neužtikrina, kad interesas bus publikuotas paskutinę kiekvieno mėnesio dieną. |
    | Visas mėnuo         | Nuomai, kurios pradžios data yra bet kada šį mėnesį, įsipareigojimų amortizavimas ir turto nuvertėjimo grafikai pradeda skaičiuoti išlaidas pirmą to mėnesio dieną. Ši lizingo sutarti užtikrina, kad interesas būtų apskaičiuotas paskutinę kiekvieno mėnesio dieną už visą mėnesį. |

3. Pasirinkite **Įrašyti**.

Sukūrus nuomą, kiekvienos knygos pradžios diena yra automatiškai įvedama pagal pradžios dieną, kuri įvedama už nuomą ir nuomos sutartį nurodytą knygoje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
