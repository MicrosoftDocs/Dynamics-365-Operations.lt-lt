---
title: Produkto gyvavimo ciklo būsenos ir perlaidos
description: Šiame straipsnyje paaiškinama, kaip galima valdyti, kurios operacijos leidžiamos kiekvienai ciklo būsenai, kai inžinerijos produktas patenka į jo ciklą.
author: t-benebo
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dd9155f799c66e8297b93d8ffbeeced1acd14220
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867962"
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
> Inžinerijos produktai naudoja tas pačias produkto gyvavimo ciklo būsenas kaip standartiniai (ne inžinerijos) produktai. Taip pat galite atidaryti produkto **ciklo būsenos puslapį**, kuris aprašytas šiame straipsnyje, **\> nueikite į produkto informacijos valdymą Nustatymo \> produkto ciklo būsena**. Dėl išsamesnės informacijos apie produkto gyvavimo ciklo būsenas, tiek inžinerijos, tiek ir standartinių produktų, žr. [Produkto gyvavimo ciklo būsenos apžvalga](../pim/product-lifecycle.md).

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
| Numatytieji parametrai išleidžiant į juridinį asmenį | Standartiniams produktams, nustatykite parinktį į *Taip*, jei gyvavimo ciklo būsena turi būti taikoma visiems produktams pagal nutylėjimą kai jie išleisti pirmą kartą. Nustatykite jį į *Ne* jei ši gyvavimo ciklo būsena bus taikoma vėliau rankiniu būdu.<p>Šie nustatymai nėra taikomi inžinerijos produktams. Inžinerijos produkto versijos gyvavimo ciklo būsena po jos sukūrimo inžinerijos įmonėje yra nurodyta jos inžinerijos keitimo kategorijoje. Paleidus produktą veikiančioje įmonėje, produkto gyvavimo ciklo būsena yra nukopijuojama. Kitaip tariant, kai inžinerijos produktas išleidžiamas į veikiančią įmonę, jis turi tą pačią gyvavimo ciklo būseną, kurią turėjo inžinerijos įmonė. Gyvavimo ciklo būsena gali būti užrašyta veikiančioje įmonėje.</p> |
| Galima planuoti | Nustatykite šią parinktį į *Taip* tam, kad ji apimtų produktus esančius šioje gyvavimo ciklo būsenoje apskaičiavimuose pagrindiniame planavime ir važtaraščio (KS) lygyje. Nustatykite jį į *Ne* tam, kad neapimtų produktų esančių šioje gyvavimo ciklo būsenoje iš skaičiavimų. |

### <a name="enabled-business-processes-fasttab"></a>Įjungti verslo procesai „FastTab“

Naudokite **Įjungti verslo procesai** „FastTab“ siekiant kontroliuoti, kurie esami verslo procesai gali būti naudojami su produktais esamoje gyvavimo ciklo būsenoje. Šiame „FastTab“ esantys procesai yra automatiškai randami tokiu būdu:

- Pirmą kartą, kai įrašote naują gyvavimo ciklo būseną, puslapis įkelia verslo procesus, kurie šiuo metu yra prieinami.
- Jei įtraukiate naujus verslo procesus į savo sistemą, galite naujinti sąrašą **Įjungti verslo procesai** „FastTab“ esamai gyvavimo ciklo būsenai pasirinkę **TIkrinti naujinimams** veiksmų juostoje.

Tolesni laukeliai yra prieinami kiekvienam procesui, kuris išvardytas **Įjungti verslo procesai** „FastTab“.

| Laukas | aprašymas |
|---|---|
| Apdoroti | Šis tik skirtas skaityti laukelis rodo esamo verslo proceso pavadinimą. |
| Proceso sritis | Šis tik skirtas skaityti laukelis rodo esamo verslo proceso sritį. |
| Polisas | Pasirinkite vieną iš tolesnių verčių, kad valdytumėte, ar ir kaip esamas procesas leis produktus esančius jų gyvavimo ciklo būsenoje:<ul><li>**Įjungta** – Verslo procesas leidžiamas.</li><li>**Blokuotas** – Procesas neleidžiamas. Jei vartotojas bando naudoti procesą produkte, kuris yra gyvavimo ciklo būsenos, sistema užblokuos bandymą ir rodys klaidą. Pavyzdžiui, galite užblokuoti iki gyvavimo galo esančius produktus neleisdami jų įsigyti.</li><li>**Įjungti su įspėjimu** – Procesas leidžiamas, bet rodomas įspėjimas. Pavyzdžiui, galbūt jums reikės, kad produkto prototipas būtų padėtas į prekybos užsakymą, kuris yra sukurtas mokslo ir vystymo skyriaus. Nepaisant to, kiti skyriai turėtų žinoti, kad jie neturėtų gaminti gaminio.</li></ul> |

Jei įtraukiate daugiau gyvavimo ciklo būsenos taisyklių į savo tinkinimą, galite peržiūrėti šias taisykles vartotojo sąsajoje (UI) pasirinkę **Naujinti procesus** viršutinėje juostoje. Mygtukas **Naujinti procesus** yra prieinamas tik administratoriams.

## <a name="lifecycle-states-for-released-products-and-product-variants"></a>Išleistų produktų ir produkto variantų ciklo valstybių narių

Produkto, kuris turi variantų (bendrasis ir variantas), produkto (bendrasis) būsena bus cikle, o kiekvieno varianto būsena gali būti skirtinga.

Jei tam tikras procesas yra užblokuotas arba variantas, arba produktas, procesas taip pat bus užblokuotas. Tiksliau, sistema patikrins, ar procesas užblokuotas:

- Inžinerijos valdomi produktai:
  - Jei dabartinė inžinerijos versija yra užblokuota, užblokuokite procesą.
  - Jei dabartinė inžinerijos variantas yra užblokuotas, užblokuokite procesą.
  - Jei leidžiamas produktas yra užblokuotas, užblokuokite procesą.
- Standartiniams produktams:
  - Jei dabartinė inžinerijos variantas yra užblokuotas, užblokuokite procesą.
  - Jei leidžiamas produktas yra užblokuotas, užblokuokite procesą.

Pavyzdžiui, tarkime, jūs norite parduoti tik vieną tam produkto variantą (raudonas) (marškinėlių) ir blokuoti visų kitų variantų pardavimą dabar. Tai galite įdiegti naudodami šiuos nustatymus:

- Priskirkite produktą ciklo būsenai, kuri leidžia procesą. Pavyzdžiui, priskirkite marškinėlių produktą kaip pardavimo ciklo *būseną* kuri leidžia pardavimo užsakymo *verslo procesui*.
- Priskirkite parduodamą variantą ciklo būsenai, kuri leidžia procesą. Pavyzdžiui, taip pat priskirkite raudoną variantą pardavimo ciklo *būsenai*.
- Visiems kitiems variantams priskirti kitą ciklo būseną, kai procesas užblokuotas. Pvz., priskirkite baltą variantą (ir visus kitus variantus) pagal ciklo būseną Parduoti negalima, o tai *neleidžia* pardavimo užsakymo *verslo proceso*.

## <a name="default-product-lifecycle-states"></a>Numatytosios produkto ciklo valstijos

Numatytoji inžinerijos versijos ciklo būsena nurodyta jos inžinerijos kategorijoje. Būsena bus numatyta kuriant naują inžinerijos versiją, įskaitant pirmąją naujo produkto versiją.

Kai kuriate naują produktą arba inžinerijos produktą, taip pat galite nustatyti numatytąją ciklo būseną, nurodydami jį produktui priskirtos paleidimo strategijos šablone išleistame produkte.

Šiuo atveju, kuriant naują inžinerijos produktą, produkto ciklo būsena gali skirtis nuo versijos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
