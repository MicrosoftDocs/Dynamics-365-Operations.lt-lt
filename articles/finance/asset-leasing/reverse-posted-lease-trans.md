---
title: Užregistruotų nuomos operacijų atšaukimas
description: Šioje temoje paaiškinama, kaip atšaukti užregistruotą nuomos operaciją. Bet kokia operacija, sukurta naudojant turto nuomą, gali būti atšaukta.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseLeaseTransactions
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1f45a06464962098f8ed98de5ae15080a778ce97
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724959"
---
# <a name="reverse-posted-lease-transactions"></a>Užregistruotų nuomos operacijų atšaukimas

[!include [banner](../includes/banner.md)]

Bet kokia operacija, sukurta naudojant turto nuomą, gali būti atšaukta. Operacijos, kurios atšaukiamos naudojant turto nuomos informaciją. Todėl jie taip pat atnaujina nuomos įsipareigojimo ir naudojimo teise valdomo turto balansinę vertę.

Norėdami sukurti nuomos operaciją, atlikite šiuos veiksmus.

1. Puslapyje **Turto operacijos** arba **Įsipareigojimų operacijos** pasirinkite operaciją ir pasirinkite **Atšaukti operaciją**.
2. Pasirodžiusiame dialogo lange galite redaguoti atšaukiamos įrašo registravimo datą. Pagal numatytuosius parametrus kopijas **Data** nustatomas į operacijos, kurią pasirinkote, operacijos registravimo datą. Atšaukiamos įrašo negalima registruoti anksčiau nei pradinė pasirinkto operacijos registravimo data.
3. Pasirinkite **Gerai**. Užregistruojamas žurnalo įrašas, kuris anuliuoja jūsų pasirinkto įrašo įrašą. Atšaukimas rodomas puslapyje **Turto operacijos** ar **Įsipareigojimų operacijos**, o grynoji dabartinio balanso suma, rodoma puslapyje, atnaujinama.

Pasirinkus **Atšaukti sekimą**, pasirodo langas, rodantis pradines operacijas ir atšauktas operacijas, kartu su susijusiu numeriu, kuris žinomas kaip *sekimo numeris*. Norėdami, kad pakeitimai būtų suprantamesni, taip pat galite sekti mažinimo naudodami nuomos grafikus.

Laukas **Naujausias žurnalo numeris** puslapyje **Grafikas** rodo operacijų žurnalų numerius. Kai operacija atšaukiama, šis laukas atnaujinamas, naudojant atšaukiamos operacijos žurnalo numerį. Be to, žymės langelis **Atšaukta** pasirenkamas, kad būtų galima nurodyti, jog operacija atšaukiama, o pasirenkamas laukas **Užregistruota**.

## <a name="revoke-a-reversed-transaction"></a>Atšauktos operacijos anuliavimas

Norėdami atšaukti atšauktą operaciją, atlikite šiuos veiksmus.

1. Puslapyje **Grafikas** arba puslapyje **Operacijos** pasirinkite pradinę operaciją.
2. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei pasirinkote operaciją puslapyje **Grafikas**, atlikite žurnalo kūrimo veiksmus iš temos [Paketinis mėnesio žurnalo įrašų kūrimas](create-monthly-journals-batch.md). Žurnalą turite registruoti neautomatiniu būdu.
    - Jei puslapyje **Operacijos** pasirinkote operaciją, pasirinkite **atšaukti operaciją**. Gausite pranešimą, kuriame nurodoma, kad šis atšaukimas yra ankstesnio atšaukimo atšaukimas ir kad galite redaguoti šio atšaukimo registravimo datą. Tačiau bendri verslo tikrinimai turi įtakos datoms, kurias galima įvesti į lauką **Data**. 

3. Pasirinkite **Gerai**. Užregistruojamas žurnalo įrašas, kuris anuliuoja jūsų pasirinkto įrašo įrašą. Atšaukimas rodomas puslapyje **Operacijos**, o grynasis visas dabartinis balansas atkuriamas iki pirmo atšaukimo. Todėl poveikis, kurį atšaukė balansai, neigiamas.

Pasirinkus **Atšaukti sekimą**, pasirodo langas, rodantis pradines operacijas ir atšauktas operacijas, kartu su sekimo numeriu.

Taip pat galite sekti atšaukimus naudodami atitinkamus puslapį **Grafikai**. Laukas **Atšaukti** panaikintas, o laukas **Žurnalas užregistruotas** yra pasirinktas. Be to, laukas **Naujausias žurnalo numeris** atnaujinamas naudojant atšaukimo operacijos žurnalo numerį, o laukas **Žurnalo numeris** atnaujinamas, atšaukiant žurnalo numerį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
