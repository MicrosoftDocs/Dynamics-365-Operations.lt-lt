---
title: Kurti ir įsigyti turtą iš mokėtinų sumų
description: Šis užduočių vadovas apžvelgs ilgalaikio turto sukūrimą ir įsigyjimą, naudojant pirkimo procesą.
author: saraschi2
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025639e6e5bdc6b95e9c496f11f29ed8ec8d388c
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914681"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Kurti ir įsigyti turtą iš mokėtinų sumų

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas apžvelgs ilgalaikio turto sukūrimą ir įsigyjimą, naudojant pirkimo procesą.  Jis naudoja buhalterio ir mokėtinų sumų tarnautojus bei demonstracinę įmonę USMF.


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

