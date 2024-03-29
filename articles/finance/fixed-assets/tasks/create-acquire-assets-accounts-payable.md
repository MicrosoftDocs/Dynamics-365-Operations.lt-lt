---
title: Kurti ir įsigyti turtą iš mokėtinų sumų
description: Ši procedūra padeda sukurti ir įsigyti ilgalaikį turtą, naudojant pirkimo procesą.
author: moaamer
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4290ced6bcf4432583cffc9122a4bba86266a559
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713619"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Kurti ir įsigyti turtą iš mokėtinų sumų

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda sukurti ir įsigyti ilgalaikį turtą, naudojant pirkimo procesą.  Jis naudoja buhalterio ir mokėtinų sumų tarnautojus bei demonstracinę įmonę USMF.


## <a name="set-fixed-assets-parameters"></a>Nustatyti ilgalaikio turto parametrus
1. **Naršymo sritis** eikite į **Moduliai > Ilgalaikis turtas > Sąranka > Ilgalaikio turto parametrai**.
2. Išplėskite „fastTab“ **Pirkimo užsakymai**.
3. Pažymėkite žymės langelį **Leisti turto įsigijimą iš pirkimo**.
4. Pažymėkite žymės langelį **Kurti turtą gaunant produktą arba registruojant sąskaitą faktūrą**.

## <a name="create-a-new-vendor-invoice"></a>Kurti naują tiekėjo SF
1. **Naršymo sritis** eikite į **Moduliai > Mokėtinos sumos > Darbo sritys > Tiekėjo sąskaitos faktūros įrašas**.
2. Spustelėkite **Nauja tiekėjo sąskaita**.
3. Lauke **Sąskaitos faktūros sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke **Numeris** įveskite vertę.
6. Lauke **Registravimo data** įveskite datą.
7. Spustelėkite **Pridėti eilutę**.
8. Lauke **Prekės numeris** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Norint įsigyti ilgalaikio turto, galima naudoti atsargose nelaikomų prekių arba įsigijimo kategorijas.  
9. Sąraše spustelėkite saitą pasirinktoje eilutėje.
10. Lauke **Kiekis** įveskite skaičių. Viena SF eilutė sukurs tik vieną ilgalaikį turtą, neatsižvelgiant į kiekį. Į ilgalaikio turto kiekį bus perkelta SF kiekio lauko reikšmė.  
11. Lauke **Vieneto kaina** įveskite skaičių.
12. Išplėskite FastTab **Eilutės informacija**.
13. Spustelėkite skirtuką **Ilgalaikis turtas**.
14. Pažymėkite žymės langelį **Kurti naują ilgalaikį turtą**.
15. Lauke **Ilgalaikio turto grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
16. Sąraše pasirinkite ilgalaikio turto grupę, kuri bus naudojama kuriant naująjį ilgalaikį turtą.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Spustelėkite **Registruoti.** Ilgalaikis turtas bus sukurtas ir įsigytas užregistravus SF.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
