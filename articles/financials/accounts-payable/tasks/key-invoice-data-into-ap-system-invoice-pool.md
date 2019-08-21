---
title: Pagrindiniai SF duomenys AP sistemoje naudojant SF telkinį
description: Šis užduočių vadovas parodys, kaip naudoti registrą kurti SF.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843222"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Pagrindiniai SF duomenys AP sistemoje naudojant SF telkinį

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas parodys, kaip naudoti registrą kurti SF.  Tada naudodami SF telkinį sugretinkite SF su pirkimo užsakymu ir baikite išlaidas tiekėjo SF puslapyje.


## <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas
1. Eikite į Mokėtinos sumos > Pirkimo užsakymai > Pirkimo užsakymai.
2. Spustelėkite Naujas, kad sukurtumėte pirkimo užsakymą.
3. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Iš sąrašo pasirinkite tiekėją. Pavyzdžiui, tiekėją 1001.
5. Spustelėkite Gerai.
6. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite paslaugų prekės numerį. Pavyzdžiui, pasirinkite S0001.
8. Spustelėkite ant prekės numerio ir jį pasirinkite.
    * Grynoji suma yra 75,00.  Tai suma, kurios tikėsimės SF.  
9. Veiksmų srityje spustelėkite Pirkti.
10. Spustelėkite Patvirtinti.

## <a name="create-and-post-and-invoice"></a>Kurti ir registruoti SF
1. Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF registras.
2. Spustelėkite Naujas.
3. Atidarykite peržvalgą, kad pasirinktumėte norimo naudoti SF registro pavadinimą.
4. Pasirinkite norimo naudoti SF registro pavadinimą.
5. Spustelėdami Eilutės atidarykite registrą ir įveskite išlaidų eilutes.
6. Peržvalgoje pasirinkite tiekėją. Pavyzdžiui, spustelėkite ant tiekėjo 1001.
7. Lauke Sąskaita faktūra įveskite SF numerį.
8. Lauke Aprašas surinkite reikšmę.
9. Lauke Kreditas įveskite skaičių.
10. Lauke Pirkimo užsakymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Pasirinkite savo anksčiau sukurtą pirkimo užsakymą.
12. Lauke Patvirtino spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
13. Pažymėkite tvirtintoją ir spustelėkite Pasirinkti, kad tą tvirtintoją pasirinktumėte.
14. Spustelėkite Registruoti.
15. Uždarykite formą.
16. Uždarykite formą.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Atidarykite SF iš telkinio ir sugretinkite ją su pirkimo užsakymu, kad užbaigtumėte SF procesą
1. Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF telkinys.
2. Spustelėkite Pirkimo užsakymas, kad iš SF telkinyje sukurtumėte tiekėjo sąskaitą faktūrą.
3. Pasirinkite sąskaitą faktūrą, kurią norite peržiūrėti.
4. Spustelėkite Naujinti gretinimo būseną, kad užbaigtumėte gretinimą.
5. Veiksmų srityje spustelėkite Parinktys.
6. Spustelėkite Keisti rodinį.
7. Spustelėkite Tinklelio rodinys.
8. Spustelėkite Registruoti.
9. Uždarykite formą.
10. Eikite į Mokėtinos sumos > Tiekėjai > Tiekėjai.
11. Pasirinkite tiekėją, kuris buvo ant pirkimo užsakymo. Pavyzdžiui, pasirinkite tiekėją 1001.
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. Veiksmų srityje spustelėkite Tiekėjas.
14. Spustelėkite Operacijos.
15. Pasirinkite savo sukurtą sąskaitą faktūrą.
    * SF registro kaupimas buvo atšauktas ir užregistruotas į atitinkamą išlaidų sąskaitą.  

