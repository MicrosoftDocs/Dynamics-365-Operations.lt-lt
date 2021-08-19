---
title: Banko žurnalo sudėtinio objekto naujinimas
description: Norėdami papildomą lauką BankTransactionType įtraukti į sudėtinį BankJournalEntity formatas, atlikite toliau nurodytus veiksmus.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cd6a1f9d7ba36e591d7e558956297781c346635c30c10d588c0dbe6d73301030
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733058"
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






[!INCLUDE[footer-include](../../includes/footer-banner.md)]