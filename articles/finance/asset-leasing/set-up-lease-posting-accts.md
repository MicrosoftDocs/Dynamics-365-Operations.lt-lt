---
title: Nuomos registravimo sąskaitų nustatymas
description: Šioje temoje išvardijamos registravimo sąskaitos, kurios būtinos turto lizingo operacijoms, ir paaiškinama, kaip nustatyti registravimo sąskaitą puslapyje Nuomos registravimo parametrai.
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
ms.openlocfilehash: 8ca1c6eea854577e5aa34b1a9b9d1731b209527b
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446182"
---
# <a name="set-up-lease-posting-accounts"></a>Nuomos registravimo sąskaitų nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje išvardijamos registravimo sąskaitos, kurios būtinos turto lizingo operacijoms, ir paaiškinama, kaip nustatyti registravimo sąskaitą puslapyje **Nuomos registravimo parametrai**.

Kad atitiktumėte apskaitos standartų kodifikavimo temą Nr. 842 (ASC 842) ir tarptautinį finansinės atskaitomybės standartą Nr. 16 (IFRS 16), jums gali tekti sukurti sąskaitų plane nurodytas sąskaitas. Tačiau jokia jūsų sukurta sąskaita, skirta laikytis ASC ir IFRS standartų, nėra ilgalaikio turto sąskaita. Pagal ASC 842, naudojimo teise valdomas turtas yra įrašomas tiek finansinei, tiek veiklos nuomai. Šios nuomos yra atskiros nuo ilgalaikio turto. (Jūs vis dar galite tvarkyti naudojimo teise valdomą turtą naudodami ilgalaikį turtą.)

Norėdami informacijos apie tai, kaip kurti sąskaitų struktūras, žr. [Sąskaitų struktūrų kūrimas](../general-ledger/tasks/create-account-structures.md). Norėdami informacijos apie tai, kaip kurti pagrindinę sąskaitą, žr. [Pagrindinės sąskaitos kūrimas](../general-ledger/tasks/create-main-account.md).

Šioje lentelėje pateikiami sąskaitų, kurias turite sukurti nuomojamoms turto operacijoms, pavyzdžiai, jei jie dar nebuvo sukurti. Pagal IFRS 16 veiklos nuomos ryšiai vis dar naudojami mažos vertės ir trumpalaikei nuomai.

| DK sąskaitos numeris | Kodo tipas  | Abonemento pavadinimas                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Ilgalaikio turto         | Transporto priemonės naudojimo teise valdomas turtas                                     |
| 180160                | Ilgalaikio turto         | Pastato naudojimo teise valdomas turtas                                    |
| 180250                | Ilgalaikio turto         | Sukauptas nusidėvėjimas – transporto priemonės                   |
| 180260                | Ilgalaikio turto         | Sukauptas nusidėvėjimas – pastatai                  |
| 222300                | Įsipareigojimai     | Trumpalaikiai įsipareigojimai – finansinė nuoma                |
| 222310                | Balanso lapas | Trumpalaikiai įsipareigojimai – veiklos nuoma              |
| 250200                | Įsipareigojimai     | Mokėtinų sumų pažymos                                         |
| 250601                | Balanso lapas | Ilgalaikiai įsipareigojimai – finansinė nuoma                 |
| 250602                | Balanso lapas | Ilgalaikiai įsipareigojimai – veiklos nuoma               |
| 250606                | Balanso lapas | Atidėtasis nuomos mokėjimas                                         |
| 300160                | Balanso lapas | Nepaskirstytas pelnas                                     |
| 604500                | Expense       | Nuomos išlaidos                                         |
| 604501                | Expense       | Transporto priemonių veiklos nuomos išlaidos – palūkanų priaugimas  |
| 604502                | Expense       | Transporto priemonių veiklos nuomos išlaidos – amortizacija        |
| 605200                | Expense       | Pastatų veiklos nuomos išlaidos – palūkanų priaugimas |
| 605201                | Expense       | Pastatų veiklos nuomos išlaidos – amortizacija       |
| 607101                | Expense       | Transporto priemonių nuomos amortizacijos išlaidos                    |
| 607102                | Expense       | Pastatų nuomos amortizacijos išlaidos                   |
| 607103                | Expense       | Nuvertėjimo išlaidos – finansinė nuoma                   |
| 607104                | Expense       | Nuvertėjimo išlaidos – veiklos nuoma                 |
| 618910                | Expense       | Nuomos išlaidos – finansinė nuoma                        |
| 618920                | Expense       | Kintamieji mokėjimai – finansinė nuoma                    |
| 618930                | Expense       | Kintamieji mokėjimai – veiklos nuoma                  |
| 800600                | Expense       | Transporto priemonių nuomos palūkanų išlaidos                        |
| 800601                | Expense       | Pastatų nuomos palūkanų išlaidos                       |
| 801201                | Balanso lapas | Pelnas ir nuostolis – nuomos modifikavimas                      |

## <a name="configure-posting-accounts"></a>Registravimo sąskaitų konfigūravimas

Norėdami priskirti sąskaitą nuomos knygoms ir grupėms, kurios buvo sukurtos, turite sukonfigūruoti turto nuomos parametrus.

1. Eikite į **Turto nuoma \> Sąranka \> Nuomos registravimo parametrai**.
2. Skirtuke **Sąskaitos** atidarykite „FastTab“ **Nuomos sąskaitos**. Nustatykite pagrindinius finansinės ir veiklos nuomos sąskaitas su atitinkamu **registravimo tipu**. Ankstesnė lentelė parodo su veiklos ir finansinės nuomos sąskaitomis susijusias sąskaita.

    > [!NOTE]
    > Atliekant šį veiksmą reikia nustatyti atskiras kiekvieno registravimo tipo sąskaitas, išskyrus sąskaitas **Nuomos išlaidų korespondentinė** ir **Nuomos padidėjimo / sumažėjimo**. Įmonės, kurios laikosi IFRS 16 apskaitos sistemos, turi pridėti pagrindinę veiklos nuomos ataskaitą. Tačiau sistema nenaudoja šios sąskaitos, net jei tai būtinas laukas, nes visos nuomos sutartys pagal IFRS 16 yra klasifikuojamos kaip finansinė nuoma.
    >[!NOTE]
    > **Nuomos padidėjimas / sumažėjimas** bus naudojamas kaip papildomo turto svarstymo, įskaitant **pradines tiesiogines išlaidas, nuomos paskatas, išankstinius nuomos mokėjimus ir išmontavimo išlaidas**, registravimo tipas, bet registruojama į naudojimo teise valdomo turto pagrindinę sąskaitą, kuri pagal numatytuosius parametrus yra **Nuomos turtas**.        
    
3. Norėdami pasirinkti konkrečią nuomos grupę, atitinkančią pagrindinę sąskaita, lauke **Sąskaitos kodas** pasirinkite **Grupė**. Tada lauke **Sąskaitos / grupės numeris** pasirinkite nuomos grupę, kurią norite priskirti pagrindinei sąskaitai.
4. Norėdami priskirti sąskaitų kodus administracinėms išlaidoms, kurios jau nustatytos sistemoje, „FastTab“ **Eksploatavimo išlaidos** lauke **Išlaidų tipas** pasirinkite išlaidas. Tada priskirkite kiekvienai knygai naudotiną finansavimą ir operacines sąskaitą.

    > [!NOTE]
    > Pasirinktas finansavimas arba operacinė sąskaita bus debetuojama, kai užregistruojama numatyto išlaidų SF.
    > **Nuomos išlaidų korespondentinė** sąskaita bus naudojama kaip eksploatavimo išlaidų operacijų registravimo tipas, bet registruojama į nurodytą **korespondentinę sąskaitą** **eksploatavimo išlaidų apmokėjimo grafiko eilutėse** nuomos informacijoje arba nuomos knygos formoje.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]