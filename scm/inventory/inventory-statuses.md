---
title: "Atsargų būsenos"
description: "Šiame straipsnyje aprašyta, kaip galite naudoti atsargų būsenas norėdami skirstyti ir sekti atsargas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, WHSInventStatus
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21331
ms.assetid: b35f495f-de4f-48a0-9d09-4d06781d7650
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 1fcdf262ee1e7e1fbbdd0a5fed46fb1867f8d8fd
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-statuses"></a>Atsargų būsenos

Šiame straipsnyje aprašyta, kaip galite naudoti atsargų būsenas norėdami skirstyti ir sekti atsargas.

Galite naudoti atsargų būsenas, kad suskirstytumėte atsargas į kategorijas. Tada galite inicijuoti atitinkamus veiksmų, pvz., papildymą ar atidėjimo darbą. 

Štai keli pavyzdžiai, kaip galima naudoti atsargų būsenas:

-   Sukurkite turimų atsargų, gavimo operacijų ir siuntimo operacijų atsargų būseną.
-   Nurodykite numatytąją atsargų būseną sandėlio operacijoms.
-   Keisti prekių atsargų būseną prieš gavimą, gavimo metu arba kai prekės atidedamos perkeliant atsargas.
-   Naudokite atsargų būseną, kad įkainotumėte grąžinamas prekes ir planuotumėte prekių padengimą atliekant bendrąjį planavimą.

Atsargų būsena – ta viena iš dimensijų saugojimo dimensijų grupėje. Atsargų būsenos gali būti klasifikuojamos kaip pasiekiamos arba nepasiekiamos, galite naudoti parametrą **Atsargų blokavimas**, kad blokuotumėte prekes, kurių atsargų būsena yra nepasiekiama. Prekės, kurių būsena yra „blokuota“, laikomos fizinėmis atsargomis, jų negalima naudoti gamybos užsakyme, pardavimo užsakyme, perkėlimo užsakyme arba siuntimo operacijoje. 

Sandėlio prekes, kurių atsargų būsena yra „pasiekiama“ arba „nepasiekiama“, galite naudoti gavimo darbams. Pavyzdžiui, galite sukurti pasiekiamą būseną, kuri vadinasi **Parengta**, nepasiekiamą būsena, kuri vadinasi **Pažeista** ir užblokuotą būseną, kuri vadinasi **Blokuota**. Kai kuriate gaunamų arba grąžinamų prekių pirkimo užsakymą, jei kurios nors prekės yra pažeistos ar sulaužytos, galite pakeisti šių prekių atsargų būseną pirkimo užsakymo eilutėje į **Pažeista **. Gavus šias prekes, būsena automatiškai nustatoma į **Blokuota**. Jeigu nuskaitote pažeistas prekes naudodami mobilųjį įrenginį, „Microsoft Dynamics 365 for Operations“ gali naudoti vietos nurodymus ir darbo šablonus, kad parodytų informaciją apie atitinkamą vietą ar vietų diapazoną, kur galite padėti šias prekes. Jei prekės grąžinamos, puslapyje **Atsargų operacijos** sukuriamas išdavimo tipas **Rezervavimas**. 

Atlikdami siuntimo darbus naudokite prekes, kurių atsargų būsena yra „pasiekiama“. Jei turite prekių, kurių būsena yra **Sulaužyta**, ir su tokiomis prekėmis atliekamas bendrasis planavimas, prekės laikomos trūkstamomis ir atsargos automatiškai papildomos. 

Nustatę atsargų būseną, galite nustatyti svetainės, prekės ir sandėlio numatytąją atsargų būseną. Taip pat galite nustatyti numatytąją pardavimų, perkėlimų ir pirkimo užsakymų būseną. Numatytosios pardavimo užsakymų ir siuntimo perkėlimo užsakymo būsenos parinkčiai **Atsargų blokavimas** negali būti nustatyta reikšmė **Taip**. Atsargų būseną, kuri gaunama pagal numatytuosius vietos, sandėlio, prekės, pirkimo užsakymo, perkėlimo užsakymo arba pardavimo užsakymo nustatymus, galima keisti naudojant mobilųjį įrenginį arba pirkimo užsakymo, pardavimo užsakymo ar perkėlimo užsakymo eilutėje. 

Norėdami suplanuoti prekių, kurių atsargų būsena yra pasiekiama, padengimą,  pasirinkite saugojimo dimensijos parinktį **Padengimo planas dimensijomis** puslapyje **Saugojimo dimensijų grupės**. Kai atidarote vedlį **Prekės padengimas **, prekės, kurių būsena yra pasiekiama, rodomos puslapyje **Būsena**. Norėdami kurti tokių prekių padengimo parametrus, pasirinkite pasiekiamų atsargų būsenų atsargų būsenos ID. Pagal padengimo parametrus galite apskaičiuoti prekių poreikius ir prognozuoti pasiekiamų prekių pasiūlą ir paklausą bendrojo planavimo metu. Negalima kurti prekės padengimo nustatymo, kai prekės atsargų būsena „blokuota“. Arba naudodami puslapį **Prekės padengimas** sukurkite arba modifikuokite prekių padengimo parametrus.


