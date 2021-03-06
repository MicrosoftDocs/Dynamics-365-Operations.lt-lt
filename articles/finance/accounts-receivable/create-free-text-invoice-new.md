---
title: Laisvos formos sąskaitos faktūros kūrimas
description: Šioje temoje paaiškinama, kaip kurti laisvos formos SF.
author: mikefalkner
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: caebd0ba0a3863920c165e1c6a61be35bcaf1e44
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833190"
---
# <a name="create-a-free-text-invoice"></a>Laisvos formos sąskaitos faktūros kūrimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip kurti laisvos formos SF. Procedūrai atlikti naudokite demonstracinių duomenų įmonę **USMF**.

## <a name="create-a-free-text-invoice"></a>Kurti laisvos formos SF

1. Eikite į **Gautos paskyros (ar pardavimų sąskaitų knyga) \> Sąskaitos \> Visos nemokamo teksto sąskaitos**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento sąskaita** pasirinkite reikšmę.

    * Pagal numatytuosius parametrus paskyra, pasirinkta kaip kliento sąskaita, naudojama kaip SF sąskaita.
    * Jei SF neužregistruota, pirmoji apskaitos būsena yra **Vykdoma**.
    * SF numeris bus priskirtas užregistravus SF.
    * Jei naudojate bendros mokėjimų eurais erdvės (SEPA) įgaliojimus, jums pasirinkus kliento sąskaitą, tiesioginio debeto įgaliojimas įvedamas automatiškai.

4. Lauke **Aprašas** įveskite reikšmę.
5. Lauke **Pagrindinė sąskaita** nurodykite sąskaitos numerį be dimensijų. Dimensijas įvesite vėliau šioje temoje.

    Norėdami rasti savo sąskaitą, taip pat galite įvesti vieną ar kelis pagrindinės sąskaitos simbolius ir naudoti peržvalgą.

6. Pasirinkite „FastTab“ **Eilutės informacija**, kad į pagrindinę sąskaitą įtrauktumėte dimensijų.
7. Pasirinkite skirtuką **Finansinių dimensijų eilutė**.

    * Nurodytos tik pasirinktos eilutės dimensijos.
    * PVM grupė užpildoma iš kliento duomenų. Jei klientas neturi PVM grupės, naudojama PVM grupė iš pagrindinės sąskaitos.
    * Prekių PVM grupė automatiškai užpildoma pagal pagrindinę sąskaitą. Jei pagrindinė sąskaita neturi prekių PVM grupės, naudojama prekių PVM grupė, nurodyta DK PVM parametruose.

8. Pasirinktinai: lauke **Kiekis** įveskite skaičių.
9. Pasirinktinai: Lauke **Vieneto kaina** įveskite skaičių.

    Suma skaičiuojama kaip kiekis, padaugintas iš vieneto kainos. Tačiau to skaičiavimo galite nepaisyti įvesdami sumą.

10. Pasirinkite **PVM**, kad peržiūrėtumėte apskaičiuotą SF PVM.

    Galite peržiūrėti PVM sumas šiame puslapyje, arba galite pakeisti sumas skirtuke **Koregavimas**.

11. Pasirinkite **Gerai**.
12. Pasirinkite **Išlaidos**, kad į SF įtrauktumėte išlaidas.
13. Lauke **Išlaidų kodas** įveskite reikšmę.
14. Lauke **Išlaidų vertė** įveskite skaičių.
15. Uždarykite puslapį.
16. Pasirinkę **Bendrosios sumos**, galėsite peržiūrėti suvestinės SF informaciją ir bendrąsias sumas.
17. Pasirinkite **Uždaryti**.
18. Pasirinkite **Registruoti**, kad užregistruotumėte SF. Vis dar turėsite galimybę atšaukti prieš užregistruodami faktiškai.

    * Galite pakeisti SF spausdinimo laiką. Pasirinkite **Dabartinis**, kad būtų spausdinama kiekviena sąskaita faktūra ją atnaujinus. Pasirinkite **Vėliau**, norėdami spausdinti, kai atnaujinamos visos sąskaitos faktūros.
    * Norėdami keisti tai, kaip kliento kredito limitas yra tikrinamas prieš registruojant SF, pakeiskite reikšmę lauke **Kredito limito tipas**.
    * Norėdami spausdinti SF, nustatykite parinktį į **Taip**.
    * Norėdami registruoti SF, nustatykite parinktį į **Taip**. Galite spausdinti SF jos neregistruodami.

19. Pasirinkite **Gerai**.

## <a name="copy-lines"></a>Kopijuoti eilutes
Norėdami kopijuoti laisvos formos sąskaitos faktūros eilutes, pasirinkite vieną ar kelias eilutes, tada pasirinkite **Kopijuoti pasirinktas eilutes**. Galite nurodyti kopijų skaičių, taip pat galite kopijuoti pastabas ir priedus. Paskirstymus galite kopijuoti arba leisti juos sukurti iš naujo registruojant.

Nukopijavę eilutes, galite pagal poreikį redaguoti informaciją.

## <a name="create-a-free-text-invoice-from-a-template"></a>Laisvos formos sąskaitos faktūros kūrimas pagal šabloną
Laisvos formos sąskaitą faktūrą galite kurti pagal šabloną. Skirtuke **Sąskaita faktūra** pasirinkę **Nauja pagal šabloną**, galite pasirinkti naujosios laisvos formos sąskaitos faktūros šablono pavadinimą ir kliento sąskaitą. Numatytąsias reikšmes, pvz., mokėjimo sąlygas ir kliento mokėjimo būdą, galima automatiškai užpildyti iš kliento duomenų arba galima naudoti šablone įrašytas reikšmes.

Bus sukurta nauja laisvos formos SF ir galėsite redaguoti norimas reikšmes.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]