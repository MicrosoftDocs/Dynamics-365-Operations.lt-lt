---
title: Atsargų būsenos
description: Šiame straipsnyje aprašyta, kaip galite naudoti atsargų būsenas norėdami skirstyti ir sekti atsargas.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus, WHSWarehouseStatusChange
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b5e693bc1c9f4b822543d812f722bc8ea9f7025
ms.sourcegitcommit: ee7a890e3e4ed6436898e5ab6eff309082a073f8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2021
ms.locfileid: "5476704"
---
# <a name="inventory-statuses"></a>Atsargų būsenos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašyta, kaip galite naudoti atsargų būsenas norėdami skirstyti ir sekti atsargas.

## <a name="set-up-and-use-inventory-statuses"></a>Nustatyti ir naudoti inventoriaus būsenas

Galite naudoti atsargų būsenas, kad suskirstytumėte atsargas į kategorijas. Tada galite inicijuoti atitinkamus veiksmų, pvz., papildymą ar atidėjimo darbą.

Štai keli pavyzdžiai, kaip galima naudoti atsargų būsenas:

- Sukurkite turimų atsargų, gavimo operacijų ir siuntimo operacijų atsargų būseną.
- Nurodykite numatytąją atsargų būseną sandėlio operacijoms.
- Keisti prekių atsargų būseną prieš gavimą, gavimo metu arba kai prekės atidedamos perkeliant atsargas.
- Naudokite atsargų būseną, kad įkainotumėte grąžinamas prekes ir planuotumėte prekių padengimą atliekant bendrąjį planavimą.

Atsargų būsena – ta viena iš dimensijų saugojimo dimensijų grupėje. Atsargų būsenos gali būti klasifikuojamos kaip pasiekiamos arba nepasiekiamos, galite naudoti parametrą **Atsargų blokavimas**, kad blokuotumėte prekes, kurių atsargų būsena yra nepasiekiama. Prekės, kurių būsena yra „blokuota“, laikomos fizinėmis atsargomis, jų negalima naudoti gamybos užsakyme, pardavimo užsakyme, perkėlimo užsakyme arba siuntimo operacijoje.

Sandėlio prekes, kurių atsargų būsena yra „pasiekiama“ arba „nepasiekiama“, galite naudoti gavimo darbams. Pavyzdžiui, galite sukurti pasiekiamą būseną, kuri vadinasi *Parengta*, nepasiekiamą būsena, kuri vadinasi *Pažeista* ir užblokuotą būseną, kuri vadinasi *Blokuota*. Kai kuriate gaunamų arba grąžinamų prekių pirkimo užsakymą, jei kurios nors prekės yra pažeistos ar sulaužytos, galite pakeisti šių prekių atsargų būseną pirkimo užsakymo eilutėje į *Pažeista*. Gavus šias prekes, būsena automatiškai nustatoma į *Blokuota*. Jeigu nuskaitote pažeistas prekes naudodami mobilųjį įrenginį, „Supply Chain Management“ gali naudoti vietos nurodymus ir darbo šablonus, kad parodytų informaciją apie atitinkamą vietą ar vietų diapazoną, kur galite padėti šias prekes. Jei prekės grąžinamos, puslapyje **Atsargų operacijos** sukuriamas išdavimo tipas *Rezervavimas*.

> [!NOTE]
> Negalima pakeisti atsargų būsenos tose vietose, kuriose yra atidarytas darbas. Pavyzdžiui, jei prekę pažymėjote kaip pirkimo gavimą, tačiau neatlikote atidėjimo veiksmo, priimančioje vietoje darbas bus pažymėtas kaip atviras ir gausite klaidos pranešimą, jei bandysite pakeisti atsargų būseną toje vietoje. Užbaigdami arba atšaukdami susijusį darbą galėtumėte pakeisti būseną.
 
Atlikdami siuntimo darbus naudokite prekes, kurių atsargų būsena yra „pasiekiama“. Jei turite prekių, kurių būsena yra *Sulaužyta*, ir su tokiomis prekėmis atliekamas bendrasis planavimas, prekės laikomos trūkstamomis ir atsargos automatiškai papildomos.

Nustatę atsargų būseną, galite nustatyti svetainės, prekės ir sandėlio numatytąją atsargų būseną. Taip pat galite nustatyti numatytąją pardavimų, perkėlimų ir pirkimo užsakymų būseną. Numatytosios pardavimo užsakymų ir siuntimo perkėlimo užsakymo būsenos parinkčiai **Atsargų blokavimas** negali būti nustatyta reikšmė *Taip*. Atsargų būseną, kuri gaunama pagal numatytuosius vietos, sandėlio, prekės, pirkimo užsakymo, perkėlimo užsakymo arba pardavimo užsakymo nustatymus, galima keisti naudojant mobilųjį įrenginį arba pirkimo užsakymo, pardavimo užsakymo ar perkėlimo užsakymo eilutėje.

Norėdami suplanuoti prekių, kurių atsargų būsena yra pasiekiama, padengimą, pasirinkite saugojimo dimensijos parinktį **Padengimo planas dimensijomis** puslapyje **Saugojimo dimensijų grupės**. Kai atidarote vedlį **Prekės padengimas**, prekės, kurių būsena yra pasiekiama, rodomos puslapyje **Būsena**. Norėdami kurti tokių prekių padengimo parametrus, pasirinkite pasiekiamų atsargų būsenų atsargų būsenos ID. Pagal padengimo parametrus galite apskaičiuoti prekių poreikius ir prognozuoti pasiekiamų prekių pasiūlą ir paklausą bendrojo planavimo metu. Negalima kurti prekės padengimo nustatymo, kai prekės atsargų būsena „blokuota“. Arba naudodami puslapį **Prekės padengimas** sukurkite arba modifikuokite prekių padengimo parametrus.

## <a name="change-inventory-statuses"></a>Keisti inventoriaus būsenas

Galite keisti inventoriaus būsnas naudodami **Turimos vietos** puslapį arba naudodami *Inventoriaus būsenos keitimo* periodinę užduotį.

- Naudodami *Inventoriaus būsenos keitimo* periodinę užduotį galite pasirinkti, kurie įrašai bus įtraukiami ir nustatyti užduotų vykdymui krūvoje pasirinktu intervalu.
- Norėdami keisti inventoriaus būseną kaip iš anksto nustatytą procesą, eikite į **Turima pagal vietą** puslapį, pasirinkite atitinkamus įrašus ir tada rinkitės **Inventoriaus būsenos keitimo** mygtuką.

> [!NOTE]
> *Inventoriaus būsenos prekių valdomų keitimas pagal sekimo matmenis* funkcija jums leidžia keisti inventoriaus kontroliuojamų prekių būseną pagal sekimo matmenis, įskaitant galimybę naujinti tik pasirinktus įrašus. Naudokite [funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad įjungtumėte funkciją kaip būtina. Funkciją įjungus, galėsite atlikti šiuos veiksmus:
>
> - Puslapyje **Turima pagal vietą** galite grupuoti eilutes pagal rodomus matmenis naudodami **Rodomi matmenys** mygtuką ir keisti pasirinktų eilučių būseną.
> - Puslapyje **Turima pagal vietą** puslapyje galtie pasirinkti keletą įrašų ir tada naudoti **Inventoriaus būsenos keitimo** mygtuką, kad pakeistumėte visus juos vienu metu.
> - Periodinėje **Inventoriaus būsenos keitimo** užduotyje galite filtruoti pagal sekimo matmenis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
