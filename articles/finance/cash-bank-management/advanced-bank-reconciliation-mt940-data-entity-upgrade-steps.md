---
title: Pažangaus banko suderinimo MT940 importavimas – Sudėtinis duomenų objekto atnaujinimas
description: Į banko išrašo importavimo objektą reikia įtraukti eilės numerį, kad būtų palaikomas MT940 formatas.
author: panolte
manager: AnnBe
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 65970cdac114b72363d2fbbc08766c99ace00b88
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445933"
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