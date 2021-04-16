---
title: Išankstinės „Commerce“ SF (Rytų Europa)
description: Šioje temoje paaiškinama, kaip nustatyti išankstinius Rytų Europos „Commerce“ pranešimus.
author: epopov
ms.date: 10/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7bdd1d99ffbc1112226fd2db168cc5fc61615b9a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798837"
---
# <a name="advance-invoices-for-commerce-for-eastern-europe"></a>Išankstinės „Commerce“ SF (Rytų Europa)

[!include [banner](../includes/banner.md)]

Šioje temoje pateikta informacija taikoma atliekant lokalizavimą Rytų Europoje ir yra susijusi su prekybos verslu.

Jei Lenkijoje, Vengrijoje ir Čekijos Respublikoje išankstinis apmokėjimas iš kliento gaunamas naudojantis elektroniniu kasos aparatu (EKA), išankstinį apmokėjimą būtina užregistruoti mokesčių tikslais ir būtina sukurti ir atsispausdinti išankstinės SF dokumentą, kuriame nurodyta išankstinio apmokėjimo suma. Be to, Lenkijoje atliekamos išankstinės SF operacijos turi būti registruojamos didžiojoje knygoje.

Galiausiai užregistravus pardavimo užsakymo SF, galutiniame dokumente turi būti išankstinė SF ir turi būti nurodyti visi išankstiniai mokėjimai.

Jei pardavimo užsakymus kuriate iš dalies Gautinos sumos, pasinaudodami dalyje [Išankstinės SF, skirtos Rytų Europai](https://docs.microsoft.com/dynamics365/unified-operations/financials/localizations/emea-advance-invoice) nurodyta procedūra, turite būtinai patys sukurti išankstines SF. Pardavimo užsakymus kuriant naudojantis EKA, išankstines SF sukuria ir užregistruoja sistema.

## <a name="supported-scenarios"></a>Palaikomi scenarijai

Palaikomi toliau nurodyti scenarijai:

- Sukurkite ir užregistruokite išankstinę SF.
- Pakeiskite depozito sumą. Jei klientas nusprendžia padidinti depozito sumą, išrašoma papildoma išankstinė SF. Atliekant bet kokius kitus depozito sumos pakeitimus (pavyzdžiui, jei redaguojamas kliento užsakymas) sukuriama pirmiau sukurtos išankstinės SF kredito pažyma, taip pat sukuriama nauja išankstinė SF, kuri užregistruojama nurodžius pataisytą sumą.
- Atšaukite pardavimo užsakymą, kuriame yra susietų išankstinių SF. Šiuo atveju sukuriama išankstinės SF kredito pažyma.
- Užregistruokite pardavimo užsakymo SF, kurioje yra susietų išankstinių SF. Atšaukiama su pardavimo užsakymu susieta išankstinė SF, kurioje nurodyta pardavimo SF suma. Sudengiamos išankstinės SF operacijos su išankstinės SF atšaukimo operacijomis.

## <a name="set-up-advance-invoices"></a>Išankstinių SF nustatymas

### <a name="turn-on-the-functionality-for-creating-advance-invoices"></a>Funkcijos, kuria naudojantis galima kurti išankstines SF, įjungimas

1. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**.
2. „FastTab“ skirtuko **Užsakymas** skirtuke **Kliento užsakymai** nustatykite veiksmo **Sukurti depozito išankstinę SF** parinktį **Taip**.

### <a name="define-the-parameters-for-posting-advance-invoices"></a>Išankstinių SF registravimo parametrų nurodymas

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
2. „FastTab“ skirtuko **Išankstinė SF** skirtuke **Naujiniai** nustatykite laukus **Registravimo šablonas**, **PVM grupė** ir **Prekės PVM grupė**. Jei šie laukai nustatyti teisingai, išankstinė SF užregistruojama. Jei šie laukai nenustatyti, išankstinės SF neregistruojamos.

### <a name="turn-off-posting-of-the-sales-tax-on-prepayment-journal-voucher"></a>PVM registravimo išankstinio mokėjimo žurnalo kvite išjungimas

Įjungus išankstinės SF registravimą PVM išankstinio mokėjimo žurnalo kvite registruoti negalima. Norėdami patikrinti, ar laikomasi šio reikalavimo, atlikite toliau nurodytus veiksmus.

1. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
2. „FastTab“ skirtuko **Mokėjimas** skirtuke **DK ir PVM** patikrinkite, ar toliau nurodyti laukai yra tušti arba ar nustatyta jų parinktis **Ne**:

    - Išankstinio mokėjimo žurnalo kvite nurodytas PVM
    - Registravimo šablonas su išankstinio mokėjimo žurnalo kvitu
    - Išankstinio mokėjimo mokesčių grupė
    - Prekės PVM grupė

## <a name="print-advance-invoices"></a>Išankstinių SF spausdinimas

Išankstines SF iš EKA alite spausdinti naudodamiesi „Microsoft Windows“ spausdintuvu, kuris susietas su aparatūros stotimi. Išankstinės SF iš EKA galima spausdinti dviem būdais:

- **Spausdinkite išankstinę SF pasibaigus EKA operacijai.** Jei sukurta išankstinė SF ir teisingai nustatytas „Windows“ spausdintuvas, šis veiksmas atliekamas automatiškai. Tokiu atveju spausdinama tik paskutinė su kliento užsakymu susieta išankstinė SF.
- **Iš naujo spausdinkite iš operacijų žurnalo gautą išankstinę SF.** Paspaudę **Rodyti žurnalą** atidarykite operacijų žurnalą, suraskite kliento užsakymą ir paspauskite **Spausdinti išankstinę SF**. Tokiu atveju spausdinamos visos su kliento užsakymu susietos išankstinės SF.

### <a name="set-up-a-windows-printer"></a>„Windows“ spausdintuvo nustatymas

Atlikite šiuos veiksmus, kad dokumentus būtų galima spausdinti iš EKA naudojant su aparatūros storimi sujungtą „Windows“ spausdintuvą.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> EKA sąranka \> EKA šablonai \> Aparatūros šablonai**.
2. Pasirinkite aparatūros šabloną, susietą su parduotuve, kurioje naudojamas spausdintuvas.
3. Atnaujinkite skyriaus **Spausdintuvas** arba **2 spausdintuvas** parametrus:

    - Lauke **Spausdintuvas** pasirinkite **„Windows“ tvarkyklė**.
    - Lauke **Įrenginio pavadinimas** įveskite spausdintuvo pavadinimą.

4. Eikite į **Mažmeninė prekyba ir prekyba \> Mažmeninės prekybos ir prekybos IT \> Paskirstymo grafikas**.
5. Pasirinkite užduotį **1090**, paskui paspauskite **Vykdyti dabar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]