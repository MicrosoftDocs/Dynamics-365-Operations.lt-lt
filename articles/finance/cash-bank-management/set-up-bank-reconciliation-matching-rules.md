---
title: Banko derinimo gretinimo taisyklių nustatymas
description: Šiame straipsnyje paaiškinta, kaip nustatyti derinimo gretinimo taisykles ir derinimo gretinimo taisyklių rinkinius, kad būtų lengviau atlikti banko derinimo procesą. Derinimo gretinimo taisyklės – tai rinkinys kriterijų, naudojamų filtruojant banko išrašo eilutes ir banko dokumento eilutes, kai vykdomas derinimo procesas.
author: panolte
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baea7ea7ec98c905e9ae896a8cf1e4ac54fb4a9d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899935"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Banko derinimo gretinimo taisyklių nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip nustatyti derinimo gretinimo taisykles ir derinimo gretinimo taisyklių rinkinius, kad būtų lengviau atlikti banko derinimo procesą. Derinimo gretinimo taisyklės – tai rinkinys kriterijų, naudojamų filtruojant banko išrašo eilutes ir banko dokumento eilutes, kai vykdomas derinimo procesas.

Galite nustatyti derinimo gretinimo taisykles ir derinimo gretinimo taisyklių rinkinius, kad būtų lengviau atlikti banko derinimo procesą. Suderinimo gretinimo taisyklė yra kriterijų rinkinys, naudojamas filtruojant banko išrašo eilutes ir "Dynamics 365" finansinių banko operacijų eilutes derinimo proceso metu. Norėdami nustatyti derinimo gretinimo taisykles, naudokite puslapį **Derinimo gretinimo taisyklės**. Galite nustatyti daugiau nei vieną gretinimo taisyklę ir pyslapyje **Derinimo gretinimo taisyklių rinkiniai** sukurti derinimo gretinimo taisyklių rinkinį. 

> [!NOTE] 
> Banko derinimo gretinimo taisyklės naudojamos, jei derinate elektroninį banko išrašą naudodamiesi išankstiniu banko derinimu. 

Puslapyje **Derinimo gretinimo taisyklės** galite pasirinkti, kokie veiksmai ir pasirinkimo kriterijai naudojami vykdant gretinimo taisyklę. Grupėje **Veiksmai** pasirinkite, koks veiksmas bus atliekamas vykdant gretinimo taisyklę derinimo proceso metu.  

Pagal numatytuosius parametrus, gretinimo taisyklės sutaps su pirmuoju banko dokumentu, kuris atitinka gretinimo taisyklės kriterijus. Jei keli banko dokumentai atitinka taisyklės kriterijus, parametras, kurį reikia gretinti rankiniu būdu, gali būti įjungtas nueinant į **Grynieji pinigai ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai > Banko derinimas > Reikalingas rankinis gretinimas, kai išplėstinės banko derinimo gretinimo taisyklės randa keletą dokumentų, atitinkančių sumą**.

> [!NOTE] 
> Rodomi laukai priklauso nuo to, kokią parinktį pasirinkote.

| Operacija | Aprašas   | Pasirinkus veiksmą galimi pasirinkimo kriterijai     |
|--------|---------------|----------------------------------------------------------|
| **Sugretinti su banko dokumentu**       | Kurdami kriterijus nurodykite, kaip bus gretinami banko dokumentai ir banko išrašo eilutės, kai vykdoma puslapio **Banko suderinimo darbalapis** gretinimo taisyklė. Operacijų eilutės atrenkamos pagal papildomus „FastTab“ skirtukuose nustatytus kriterijus.                                | **1 veiksmas. Apibrėžkite gretinimo taisyklę** – pasirinkite kriterijus, nurodančius, kurie banko išrašai turi būti gretinami su „“Finance“ banko operacijomis. **2 veiksmas (pasirinktinai): pasirinkite išrašo eilutes, pagal kurias turi būti vykdomos gretinimo taisyklės:** pritaikykite filtrą, nurodantį, pagal kurią išrašo eilutę vykdyti taisykles.                                                                                                                                                                                                                                                                                                               |
| **Išvalyti atšaukimo išrašo eilutes** | Kurdami kriterijus nurodykite, kaip bus gretinami banko dokumentai ir banko išrašo eilutės, kai vykdoma puslapio **Banko suderinimo darbalapis** gretinimo taisyklė. Ši parinktis naudojama, kai dėl banko klaidos importuotame banko išraše yra dvi banko išrašo eilutės, kurias reikia derinti. | **1 veiksmas**:**rasti atšaukimo išrašo eilutes**– įtraukite pasirinkimo kriterijų, pagal kuriuos pasirenkamos atšaukimo banko išrašo eilutės. Pavyzdžiui, norėdami pasirinkti tik čekius, lauke Laukas pasirinkite **Banko operacijos kodas**, lauke **Operatorius** pasirinkite pliuso ženklą (+) ir lauke Reikšmė įveskite **Čekiai**. **2 veiksmas: rasti pirminio išrašo eilutes** – galite pridėti pasirinkimo kriterijų, pagal kuriuos banko dokumento eilutės bus gretinamos su banko išrašo eilutėmis. **3 veiksmas: rasti „Finance“ banko operacijas** – galite pridėti pasirinkimo kriterijų, pagal kuriuos „Finance“ banko operacijos bus gretinamos su banko išrašo eilutėmis. |
| **Žymėti naujas operacijas**          | Kurdami kriterijus nurodykite, kaip puslapyje **Banko suderinimo darbalapis** turėtų būti žymimos naujos operacijos, kai vykdoma gretinimo taisyklė.                                                                                                                                                                 | **1 veiksmas: rasti išrašo eilutes**– įtraukite pasirinkimo laukų, kurie nurodytų, kurios puslapio **Banko suderinimo darbalapis** banko išrašo eilutės turėtų būti pasirinktos. **2 veiksmas: rasti „Finance and Operations‟** – galite įtraukti pasirinkimo kriterijų, pagal kuriuos būtų ieškoma banko dokumentų eilučių. Jei nerandamas joks banko dokumentas, išrašo eilutė bus pažymėta kaip nauja operacija.                                                                                                                                                                                                                                             |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
