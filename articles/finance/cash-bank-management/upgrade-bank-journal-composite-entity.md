---
title: Banko žurnalo sudėtinio objekto naujinimas
description: Norėdami papildomą lauką BankTransactionType įtraukti į sudėtinį BankJournalEntity formatas, atlikite toliau nurodytus veiksmus.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899647"
---
# <a name="update-the-bank-journal-composite-entity"></a>Banko žurnalo sudėtinio objekto naujinimas

[!include [banner](../includes/banner.md)]

Norėdami papildomą lauką BankTransactionType įtraukti į sudėtinį BankJournalEntity formatas, atlikite toliau nurodytus veiksmus.

Norėdami papildomą lauką BankTransactionType įtraukti į sudėtinį BankJournalEntity formatas, atlikite toliau nurodytus veiksmus.

1.  Kompiliuokite ir sinchronizuokite toliau nurodytus banko žurnalo sudėtinius objektus, objektus ir išdėstymo lenteles.
    -   Sudėtinis objektas\\BankJournalEntity
    -   Objektas\\BankJournalHeaderEntity
    -   Objektas\\BankJournalLineEntity
    -   Lentelė\\BankJournalHeaderStaging
    -   Lentelė\\BankJournalLineStaging

2.  Duomenų valdymas\\duomenų projektai
    -   Makete **Šaltinio duomenys** rodykite tipą **Banko operacija**.
        -   Šaltinio duomenų formatas = XML-Element
        -   Objekto pavadinimas = banko žurnalas
        -   Nusiuntimo duomenų failas = nauja SampleBankJournalCompositeEntity.xml versija
        -   Jei norite perrašyti esamą failą, spustelėkite **Taip**.
        -   Jeigu norite generuoti susiejimą nuo pradžių, spustelėkite **Taip**.
        -   Patikrinkite, ar banko operacijos tipas yra susietas.
            -   Objekte Eilutė spustelėkite **Peržiūrėti schemą**.
            -   Patikrinkite, ar banko operacijos tipas yra susietas nuo šaltinio iki išdėstymo.

3.  Importuokite naują išrašą.




