---
title: Pažangaus banko suderinimo MT940 importavimas – Sudėtinis duomenų objekto atnaujinimas
description: Į banko išrašo importavimo objektą reikia įtraukti eilės numerį, kad būtų palaikomas MT940 formatas.
author: panolte
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c891a5139ff7de85e6762513f57236e24f1644529d7825c9ce5e1dfda50fbad8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739388"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a>Pažangaus banko suderinimo MT940 importavimas – Sudėtinis duomenų objekto atnaujinimas

[!include [banner](../includes/banner.md)]

Į banko išrašo importavimo objektą reikia įtraukti eilės numerį, kad būtų palaikomas MT940 formatas. 

Norėdami įtraukti banko išrašo importavimo objektą, kad būtų palaikomas MT940 formatas, atlikite toliau nurodytus veiksmus.

1.  Kompiliuokite ir sinchronizuokite šiuos objektus:
    -   Sudėtinis objektas\\BankStatementImportEntity
    -   Objektas\\BankStatementBalanceEntity
    -   Objektas\\BankStatementDocumentEntity
    -   Objektas\\BankStatementEntity
    -   Objektas\\BankStatementLineEntity
    -   Lentelės\\BankStatementStaging

2.  Duomenų valdymas\\duomenų projektai.
    1.  Įkelkite MT940 importavimo projektą(-us)
        1.  Pakeiskite XSLT.
            -   Spustelėkite **Peržiūrėti schemą**.
            -   Banko išrašo dokumente spustelėkite **Peržiūrėti schema**.
            -   Spustelėkite **Pakeitimai**
            -   Panaikinkite failą BankReconiliation-to-Composite.xslt.
            -   Pridėkite naują BankReconiliation-to-Composite.xsl versiją.

        2.  Makete **Šaltinio duomenys** rodykite **Eilės numeris**.
            1.  Šaltinio duomenų formatas = XML-Element.
            2.  Objekto pavadinimas = Banko išrašai.
            3.  Nusiuntimo duomenų failas = nauja SampleBankCompositeEntity.xml versija.
            4.  Jei norite perrašyti esamą failą, spustelėkite **Taip**.
            5.  Jeigu norite sugeneruoti naują susiejimą, spustelėkite **Taip**.
            6.  Patikrinkite, ar susietas E **ilės numeris**.
                -   Išrašo objekte spustelėkite **Peržiūrėti schema**.
                -   Patikrinkite, ar objektas **SequenceNumber** susietas nuo šaltinio iki išdėstymo.

3.  Importuokite naują išrašą.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]