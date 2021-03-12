---
title: Produkto gyvavimo ciklo būsenos ir perlaidos
description: Šioje temoje paaiškinta, kaip gali valdyti perlaidas, kurioms leidžiama būti visose gyvavimo ciklo būsenos kai inžinerijos produktas eina per savo gyvavimo ciklą.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 989cfd3846e4921d24f5dcf809f1735d2cf62dbb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005332"
---
# <a name="product-lifecycle-states-and-transactions"></a>Produkto gyvavimo ciklo būsenos ir perlaidos

[!include [banner](../includes/banner.md)]

Kadangi inžinerijos produktas eina per savo gyvavimo ciklą, svarbu, kad galėtumėte valdyti, kurios perlaidos leidžiamos kiekvienoje gyvavimo ciklo būsenoje. Pavyzdžiui, produktai, kurie dar nėra subrendusios būsenos neturi būti padėti į prekybos užsakymą. Kitu atveju, jei produktas pasiekia savo gyvavimo ciklo pabaigą, jums gali reikėti valdyti to produkto įvestį.

Inžinerijos produktui, gyvavimo ciklo būsenos pakeitimai yra susiję su produkto inžinerijos versijomis. Dėl to, produkto gyvavimo ciklo būsena gali būti taip pat susieta su jo inžinerijos versijomis. Kai produkto gyvavimo ciklo būsena yra susieta su inžinerijos versija, galite naudoti gyvavimo ciklo būseną, kad valdytumėte, kurios perlaidos leidžiamos inžinerijos versijai.

## <a name="create-and-manage-product-lifecycle-states"></a>Sukurkite ir valdykite produkto gyvavimo ciklo būsenas

Tam, kad dirbtumėte su produkto gyvavimo ciklo būsenomis, eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Produkto gyvavimo ciklo būseną**. Tuomet atlikite vieną iš šių žingsnių.

- Norėdami sukurti naują gyvavimo ciklo būseną, rinkitės **Naujas** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami redaguoti esančią gyvavimo ciklo būseną, sąrašo juostoje ją pasirinkite ir rinkitės **Redaguoti** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami panaikinti esančią gyvavimo ciklo būseną, sąrašo juostoje ją pasirinkite ir rinkitės **Naikinti** veiksmų juostoje.

> [!NOTE]
> Inžinerijos produktai naudoja tas pačias produkto gyvavimo ciklo būsenas kaip standartiniai (ne inžinerijos) produktai. Galite taip pat atverti **Produkto gyvavimo ciklo būseną** puslapį, kuris aprašytas šioje temoje eidami į **Produkto informacijos valdymą \> Nustatymus \> Produkto gyvavimo ciklo būsena**. Dėl išsamesnės informacijos apie produkto gyvavimo ciklo būsenas, tiek inžinerijos, tiek ir standartinių produktų, žr. [Produkto gyvavimo ciklo būsenos apžvalga](../pim/product-lifecycle.md).

### <a name="header"></a>Antraštė

Nustatykite tolesnius laukelius produkto gyvavimo ciklo būsenos antraštėje.

| Laukas | aprašymas |
|---|---|
| Apskritis | Įveskite produkto gyvavimo ciklo būsenos pavadinimą. |
| aprašymas | Įveskite produkto gyvavimo ciklo būsenos aprašą. |

### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

Nustatykite tolesnius laukelius „FastTab“ **Bendri**.

| Laukas | aprašymas |
|---|---|
| Numatytieji parametrai išleidžiant į juridinį asmenį | Standartiniams produktams, nustatykite parinktį į *Taip*, jei gyvavimo ciklo būsena turi būti taikoma visiems produktams pagal nutylėjimą kai jie išleisti pirmą kartą. Nustatykite jį į *Ne* jei ši gyvavimo ciklo būsena bus taikoma vėliau rankiniu būdu.<p>Šie nustatymai nėra taikomi inžinerijos produktams. Inžinerijos produkto versijos gyvavimo ciklo būsena po jos sukūrimo inžinerijos įmonėje yra nurodyta jos inžinerijos keitimo kategorijoje. Paleidus produkta veikiančioje įmonėje, produkto gyvavimo ciklo būsena yra nukopijuojama. Kitaip tariant, kai inžinerijos produktas išleidžiamas į veikiančią įmonę, jis turi tą pačią gyvavimo ciklo būseną, kurią turėjo inžinerijos įmonė. Gyvavimo ciklo būsena gali būti užrašyta veikiančioje įmonėje.</p> |
| Galima planuoti | Nustatykite šią parinktį į *Taip* tam, kad ji apimtų produktus esančius šioje gyvavimo ciklo būsenoje apskaičiavimuose pagrindiniame planavime ir važtaraščio (BOM) lygyje. Nustatykite jį į *Ne* tam, kad neapimtų prodoktų esančių šioje gyvavimo ciklo būsenoje iš skaičiavimų. |

### <a name="enabled-business-processes-fasttab"></a>Įjungti verslo procesai „FastTab“

Naudokite **Įjungti verslo procesai** „FastTab“ siekiant kontroliuoti, kurie esami verslo procesai gali būti naudojami su produktais esamoje gyvavimo ciklo būsenoje. Šiame „FastTab“ esantys procesai yra automatiškai randami tokiu būdu:

- Pirmą kartą, kai įrašote naują gyvavimo ciklo būseną, puslapis įkelia verslo procesus, kurie šiuo metu yra prieinami.
- Jei įtraukiate naujus verslo procesus į savo sistemą, galite naujinti sąršą **Įjungti verslo procesai** „FastTab“ esamai gyvavimo ciklo būsenai pasirinkę **TIkrinti naujinimams** veiksmų juostoje.

Tolesni laukeliai yra prieinami kiekvienam procesui, kuris išvardytas **Įjungti verslo procesai** „FastTab“.

| Laukas | aprašymas |
|---|---|
| Apdoroti | Šis tik skirtas skaityti laukelis rodo esamo verslo proceso pavadinimą. |
| Proceso sritis | Šis tik skirtas skaityti laukelis rodo esamo verslo proceso sritį. |
| Polisas | Pasirinkite vieną iš tolesnių verčių, kad valdytumėte, ar ir kaip esamas procesas leis produktus esančius jų gyvavimo ciklo būsenoje:<ul><li>**Įjungta** – Verslo procesas leidžiamas.</li><li>**Blokuotas** – Procesas neleidžiamas. Jei vartotojas bando naudoti procesą produkte, kuris yra gyvavimo ciklo būsenos, sistema užblokuos bandymą ir rodys klaidą. Pavyzdžiui, galite užblokuoti iki gyvavimo galo esančius produktus neleisdami jų įsigyti.</li><li>**Įjungti su įspėjimu** – Procesas leidžiamas, bet rodomas įspėjimas. Pavyzdžiui, galbūt jums reikės, kad produkto prototipas būtų padėtas į prekybos užsakymą, kuris yra sukurtas mokslo ir vystymo skyriaus. Nepaisant to, kiti skyriai turėtų žinoti, kad jie neturėtų gaminti gaminio.</li></ul> |

Jei įtraukiate daugiau gyvavimo ciklo būsenos taisyklių į savo tinkinimą, galite peržiūrėti šias taisykles vartotojo sąsajoje (UI) pasirinkę **Naujinti procesus** viršutinėje juostoje. Mygtukas **Naujinti proceuss** yra prieinamas tik administratoriams.
