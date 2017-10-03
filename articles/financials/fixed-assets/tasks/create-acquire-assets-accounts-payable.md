--- 
title: "Kurti ir įsigyti turtą iš mokėtinų sumų"
description: "Šis užduočių vadovas apžvelgs ilgalaikio turto sukūrimą ir įsigyjimą, naudojant pirkimo procesą."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f814d20bc16bb3334ae4bc449cc0d45843487023
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Kurti ir įsigyti turtą iš mokėtinų sumų

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas apžvelgs ilgalaikio turto sukūrimą ir įsigyjimą, naudojant pirkimo procesą.  Jis naudoja buhalterio ir mokėtinų sumų tarnautojus bei demonstracinę įmonę USMF.


## <a name="set-fixed-assets-parameters"></a>Nustatyti ilgalaikio turto parametrus
1. Eikite į Ilgalaikis turtas > Nustatymas > Ilgalaikio turto parametrai.
2. Išplėskite arba sutraukite dalį Pirkimo užsakymai.
3. Pažymėkite žymės langelį Leisti turto įsigijimą iš pirkimo.
4. Pažymėkite žymės langelį Kurti turtą registruojant gavimo dokumentą ar SF.

## <a name="create-a-new-vendor-invoice"></a>Kurti naują tiekėjo SF
1. Pasirinkite Mokėtinos sumos > Darbo sritis > Tiekėjo SF įrašas.
2. Spustelėkite Nauja tiekėjo SF.
3. Lauke SF sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke Numeris surinkite reikšmę.
6. Lauke Registravimo data įveskite datą.
7. Spustelėkite Pridėti eilutę.
8. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Norint įsigyti ilgalaikio turto, galima naudoti atsargose nelaikomų prekių arba įsigijimo kategorijas.  
9. Sąraše spustelėkite saitą pasirinktoje eilutėje.
10. Lauke Kiekis įveskite skaičių.
    * Viena SF eilutė sukurs tik vieną ilgalaikį turtą, neatsižvelgiant į kiekį.  Į ilgalaikio turto kiekį bus perkelta SF kiekio lauko reikšmė.  
11. Lauke Vieneto kaina įveskite skaičių.
12. Išplėskite arba sutraukite dalį Išsami eilučių informacija.
13. Spustelėkite skirtuką Ilgalaikis turtas.
14. Pažymėkite žymės langelį Kurti naują ilgalaikį turtą.
15. Lauke Ilgalaikio turto grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
16. Sąraše pasirinkite ilgalaikio turto grupę, kuri bus naudojama kuriant naująjį ilgalaikį turtą.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Spustelėkite Registruoti.
    * Ilgalaikis turtas bus sukurtas ir įsigytas užregistravus SF.  


