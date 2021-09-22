---
title: „Registruoti DK mokesčių sąskaitoje” parametras nėra įjungtas
description: Ši problema atsiranda, kai pirkimo užsakymui išrašoma SF, jei pasirinktis Registruoti DK mokesčių sąskaitoje yra įjungta kaip Taip skirtuke „SF“, esančiame „Mokėtinų sumų parametrai puslapyje“.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477112"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>„Registruoti DK mokesčių sąskaitoje” parametras nėra įjungtas

## <a name="symptoms"></a>Požymiai

Ši problema atsiranda, kai pirkimo užsakymui išrašoma SF, jei pasirinktis **Registruoti DK mokesčių sąskaitoje** yra nustatyta kaip *Taip* skirtuke **SF**, esančiame **Mokėtinų sumų parametrai** puslapyje.

## <a name="reproduce-the-issue"></a>Problemos atkūrimas

Toliau aprašyta procedūra pateikia vieną būdą, kaip atkurti problemą.

1. Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.
1. **SF** skirtuke nustatykite pasirinktį **Registruoti DK mokesčių sąskaitoje** kaip *Taip*.
1. Eikite į **Atsargų valdymas \> Sąranka \> Registravimas \> Registravimas**.
1. **Pirkimo užsakymas** skirtuke įsitikinkite, kad panaikinote visas produkto pirkimo išlaidų eilutes.
1. Eikite į **Mokėtinos sumos \> Pirkimo užsakymai \> Visi pirkimo užsakymai**.
1. Sukurkite pirkimo užsakymą. **Tiekėjo sąskaita** lauke pasirinkite *1001 Acme biuro reikmenys*.
1. Pridėkite pirkimo užsakymo eilutę, kuriai nustatyti šie parametrai:

    - **Prekės numeris:** *D0011 lazerinis projektorius*
    - **Vieta:** *1*
    - **Sandėlis:** *11*
    - **Kiekis:** *4*

1. Veiksmų srities skirtuke **Pirkimas**, grupėje **Veiksmas**, pasirinkite **Patvirtinti**.
1. Veiksmų srities skirtuke **Gauti**, grupėje **Generuoti**, pasirinkite **Gavimo dokumentas**.
1. Dialogo lange **Registruojamas gavimo dokumentas**, lauke **Gavimo dokumentas**, įveskite pasirinktinį numerį ir pasirinkite **Gerai**.
1. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.
1. Lauke **Numeris** įveskite pasirinktinį numerį kaip SF numerį.
1. Atnaujinkite gretinimo būseną ir registruokite.
1. Atkreipkite dėmesį, kad kai generuojate SF iš pirkimo užsakymo, dabar gausite šią klaidą: „Produkto pirkimo išlaidų operacijos tipui sąskaitos numerio nėra.”

## <a name="resolution"></a>Sprendimas

Tai priklauso nuo SF ir SF grupių parametrų nustatymų. Norėdami gauti daugiau informacijos, žr. šį tinklaraščio įrašą: [Pirkimo mokesčio ir atsargų nuokrypio apskaita](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).
